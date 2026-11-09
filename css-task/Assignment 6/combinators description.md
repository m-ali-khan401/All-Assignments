# CSS Combinators

## What is a Combinator? | Combinator kya hota hai?

**English:** A combinator is a symbol placed between two selectors. It tells the browser what relationship the two elements must have (parent, child, sibling) for the style to apply.

**Urdu:** Combinator ek symbol hota hai jo do selectors ke beech mein lagta hai. Ye browser ko batata hai ke dono elements ka aapas mein kya rishta hona chahiye (parent, child, bhai) tab style lagay.

---

## 1. Descendant Combinator ( space )

**Syntax:** `.descombinator p { }`

**English:** Selects every element inside the parent, no matter how deep it is nested (child, grandchild, great-grandchild...).

**Urdu:** Parent ke andar maujood har element ko select karta hai, chahe wo kitna hi gehra ho (bacha, pota, pardota...).

**Example result:** `para 1` and `para 2` are both styled.

---

## 2. Child Combinator ( > )

**Syntax:** `.childcombinator > p { }`

**English:** Selects only the direct children of the parent. If another tag sits in between, the element is not selected.

**Urdu:** Sirf parent ke direct bachay select hotay hain. Agar beech mein koi aur tag aa jaye to wo element select nahi hota.

**Example result:** Only `direct` is styled. `nested` is not, because it is inside an extra div.

**Difference from Descendant:** Descendant goes through all levels, Child goes only one level.

---

## 3. Adjacent Sibling Combinator ( + )

**Syntax:** `h2 + p { }`

**English:** Selects only the one sibling that comes immediately after the given element.

**Urdu:** Kisi element ke bilkul foran baad aanay wala sirf ek bhai/behen select hota hai.

**Example result:** Only `after 1` is styled. `before` comes earlier, and `after 2` is not immediately after the h2.

---

## 4. General Sibling Combinator ( ~ )

**Syntax:** `.generalcombinator h2 ~ p { }`

**English:** Selects all siblings that come after the given element, even if other tags are in between.

**Urdu:** Kisi element ke baad aanay walay tamam bhai/behen select hotay hain, chahe beech mein koi aur tag ho.

**Example result:** `after 1` and `after 2` are styled (the span in between does not matter). `before` is not styled because it is before the h2.

**Difference from Adjacent:** `+` selects only the next one, `~` selects all that come after.

---

## Summary | Khulasa

| Combinator | Symbol | Selector used | Styled elements |
|---|---|---|---|
| Descendant | space | `.descombinator p` | para 1, para 2 |
| Child | `>` | `.childcombinator > p` | direct |
| Adjacent Sibling | `+` | `h2 + p` | after 1 |
| General Sibling | `~` | `.generalcombinator h2 ~ p` | after 1, after 2 |