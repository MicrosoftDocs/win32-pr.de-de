---
title: Konstanten Attribut
description: Das Schlüsselwort "Konstanten" ändert den Typ einer Typdeklaration oder den Typ eines Funktions Parameters, wodurch der Wert nicht unterschiedlich ist.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- Konstante Attribut-Mittel l
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724968"
---
# <a name="const-attribute"></a><span data-ttu-id="4b9d1-104">Konstanten Attribut</span><span class="sxs-lookup"><span data-stu-id="4b9d1-104">const attribute</span></span>

<span data-ttu-id="4b9d1-105">Das Schlüsselwort " **Konstanten** " ändert den Typ einer Typdeklaration oder den Typ eines Funktions Parameters, wodurch der Wert nicht unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="4b9d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9d1-107">*"Typ"-Typ*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-108">Gibt eine gültige Zeichenfolge, ein Zeichen, eine Zeichenfolge oder einen booleschen Wert für die mittlere Zahl an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="4b9d1-109">Zu den gültigen Mittel Typen zählen [**Small**](small.md), [**Short**](short.md), [**Long**](long.md) [](char-idl.md) [](byte.md) **\***, Char, Char, [**WCHAR \_**](wchar-t.md) **\_ \*** **\*** t, [**\***](void.md)WCHAR t, Byte, Byteund void.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \***, [**wchar\_t**](wchar-t.md), **wchar\_tÂ \***, [**byte**](byte.md), **byteÂ \***, and [**voidÂ \***](void.md).</span></span> <span data-ttu-id="4b9d1-110">Die ganzzahligen und Zeichen Typen können mit oder [**ohne**](unsigned.md)Vorzeichen [**signiert**](signed.md) werden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-110">The integer and character types can be [**signed**](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-112">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="4b9d1-113">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-114">*Ausdruck "Konstanten"*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-115">Gibt einen Ausdruck, einen Bezeichner oder eine numerische oder Zeichen Konstante für den angegebenen Typ an: Konstante ganzzahlige Literale oder Konstante ganzzahlige Ausdrücke für ganzzahlige Konstanten. Boolesche Ausdrücke, die bei der Kompilierung für [**boolesche**](boolean.md) Typen berechnet werden können. Einzelzeichen Konstanten für [**char**](char-idl.md) -Typen; und Zeichen folgen Konstanten für **\[** [**Zeichen**](string.md) folgen **\]** Typen.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="4b9d1-116">Der Typ [**"void" \***](void.md) kann nur mit **null** initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-116">The [**voidÂ \***](void.md) type can be initialized only to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-118">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-119">*Zeigertyp*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-120">Gibt einen gültigen Mittell-Zeigertyp an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-121">*Deklarator und Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-122">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4b9d1-123">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4b9d1-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4b9d1-124">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="4b9d1-125">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-126">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-127">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="4b9d1-128">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4b9d1-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-129">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-130">Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="4b9d1-131">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-132">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-133">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="4b9d1-134">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn **\*** Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " **Konstanten**" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the **\*** designator, modifiers such as **far**, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-135">*function-name*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-136">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-137">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4b9d1-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9d1-138">Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="4b9d1-139">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b9d1-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b9d1-140">Remarks</span></span>

<span data-ttu-id="4b9d1-141">Mithilfe von "Mittel l" können Sie Konstante Integer-, Zeichen-, Zeichen folgen-und boolesche Typen im Schnittstellen Text der IDL-Datei deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="4b9d1-142">Die **Konstanten** Typdeklarationen werden in der generierten Header Datei als **\# define** -Direktiven reproduziert.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="4b9d1-143">DCE-IDL-Compiler unterstützen keine Konstanten Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="4b9d1-144">Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="4b9d1-145">Eine zuvor definierte Konstante kann als zugewiesener Wert einer nachfolgenden Konstante verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="4b9d1-146">Der Wert eines Konstanten ganzzahligen Ausdrucks wird in Übereinstimmung mit C-Konvertierungsregeln automatisch in den entsprechenden ganzzahligen Typ konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="4b9d1-147">Der Wert einer Zeichen Konstante muss ein ASCII-Zeichen mit nur einem Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="4b9d1-148">Wenn die Zeichen Konstante das einfache Anführungszeichen (') ist, muss der umgekehrte Schrägstrich ( \) wie in ' ' vor dem einfachen Anführungszeichen stehen \\ .</span><span class="sxs-lookup"><span data-stu-id="4b9d1-148">When the character constant is the single-quote character itself ('), the backslash character (\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="4b9d1-149">Der Wert einer Zeichen folgen Konstante muss eine Zeichenfolge in doppelten Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="4b9d1-150">Innerhalb einer Zeichenfolge muss der umgekehrte Schrägstrich ( **\\** ) dem literalen doppelten Anführungszeichen ( **"** ) vorangestellt werden, wie in **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="4b9d1-151">Innerhalb einer Zeichenfolge stellt der umgekehrte Schrägstrich ( **\\** ) ein Escapezeichen dar.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="4b9d1-152">Zeichen folgen Konstanten können bis zu 255 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="4b9d1-153">Der Wert **null** ist der einzige gültige Wert für Konstanten vom Typ [**"void" \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="4b9d1-153">The value **NULL** is the only valid value for constants of type [**voidÂ \***](void.md).</span></span> <span data-ttu-id="4b9d1-154">Alle Attribute, die der **Konstanten** Deklaration zugeordnet sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-154">Any attributes associated with the **const** declaration are ignored.</span></span>

<span data-ttu-id="4b9d1-155">Der mittlerer l-Compiler überprüft bei der **Konstanten** Initialisierung keine Bereichs Fehler.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="4b9d1-156">Wenn Sie z. b. "Konstante Short x = 0xffffffff;" angeben, meldet der Mittell-Compiler keinen Fehler, und der Initialisierer wird in der generierten Header Datei reproduziert.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="4b9d1-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b9d1-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="4b9d1-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4b9d1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9d1-159">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-160">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="4b9d1-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-161">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-162">**Hobby**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-163">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-164">**Char**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-165">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-166">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-167">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="4b9d1-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-168">**lassen**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-169">**nah**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-170">**lange**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-174">**short**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-175">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-176">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-177">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-178">**struct**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-179">**Union**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-180">**gem**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-181">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-182">**void**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 