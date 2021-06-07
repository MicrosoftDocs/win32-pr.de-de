---
title: const-Attribut
description: Das schlüsselwort const ändert den Typ einer Typdeklaration oder den Typ eines Funktionsparameters, sodass der Wert nicht variiert.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- const-Attribut MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387059"
---
# <a name="const-attribute"></a><span data-ttu-id="bdbe9-104">const-Attribut</span><span class="sxs-lookup"><span data-stu-id="bdbe9-104">const attribute</span></span>

<span data-ttu-id="bdbe9-105">Das **schlüsselwort const** ändert den Typ einer Typdeklaration oder den Typ eines Funktionsparameters, sodass der Wert nicht variiert.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="bdbe9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdbe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbe9-107">*const-type*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-108">Gibt eine gültige MIDL-Ganzzahl, ein gültiges Zeichen, eine Zeichenfolge oder einen booleschen Typ an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="bdbe9-109">Gültige MIDL-Typen sind [**kleine**](small.md), [**kurze**](short.md), [**lange**](long.md), [**char**](char-idl.md), \**\* charÂ* _, _ [*wchar \_ t* \*](wchar-t.md), \**wchar \_ \* tÂ*_, _ [*byte* \*](byte.md), \**byteÂ \** _, und [_*void". \**_](void.md)</span><span class="sxs-lookup"><span data-stu-id="bdbe9-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \**_, [_ *wchar\_t*\*](wchar-t.md), \**wchar\_tÂ \**_, [_ *byte*\*](byte.md), \**byteÂ \** _, and [_*voidÂ \**_](void.md).</span></span> <span data-ttu-id="bdbe9-110">Die Ganzzahl- und Zeichentypen können [*_signed* \*](signed.md) oder [**unsigned**](unsigned.md)sein.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-110">The integer and character types can be [_ *signed*\*](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-112">Gibt einen gültigen MIDL-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="bdbe9-113">Gültige MIDL-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder Unterstrichen und müssen mit einem Alphabet- oder Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-114">*const-expression*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-115">Gibt einen Ausdruck, einen Bezeichner oder eine numerische oder Zeichenkonstante an, die für den angegebenen Typ geeignet ist: konstante ganzzahlige Literale oder konstante ganzzahlige Ausdrücke für ganzzahlige Konstanten; Boolesche Ausdrücke, die bei der Kompilierung für [**boolesche**](boolean.md) Typen berechnet werden können. Einzelzeichenkonstanten [](char-idl.md) für Char-Typen; und Zeichenfolgenkonstanten für **\[** [](string.md) **\]** Zeichenfolgentypen.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="bdbe9-116">Der [ \* *voidÂ \** _-Typ](void.md) kann nur mit _*NULL*\* initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-116">The [\**voidÂ \** _](void.md) type can be initialized only to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-118">Gibt ein oder mehrere Attribute an, die für den Typ gelten.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-119">*Zeigertyp*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-120">Gibt einen gültigen MIDL-Zeigertyp an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-121">*deklarator und declarator-list*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-122">Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="bdbe9-123">Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers)</span><span class="sxs-lookup"><span data-stu-id="bdbe9-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="bdbe9-124">Die *Deklaratorliste* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="bdbe9-125">Der Parameternamenbezeichner im Funktionsdeklarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-126">*function-attr-list*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-127">Gibt null oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="bdbe9-128">Gültige Funktionsattribute sind **\[** [**rückruf,**](callback.md) **\]** **\[** [**local,**](local.md) **\]** das Zeigerattribut **\[** [**ref,**](ref.md) **\]** **\[** [**eindeutig**](unique.md)oder **\]** **\[** [**ptr**](ptr.md)und die **\]** Verwendungsattribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**\_ Kontexthandle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bdbe9-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-129">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-130">Gibt einen [ \_ Basistyp,](midl-base-types.md) [**eine Struktur,**](struct.md) [**einen Union-,**](union.md) [**Enumerations-**](enum.md) oder Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="bdbe9-131">Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-132">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-133">Gibt null oder mehr Zeigerdeklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="bdbe9-134">Ein Zeigerdeklarator ist identisch mit dem in C verwendeten Zeigerdeklarator. Sie wird aus dem **\* *_-Bezeichner, Modifizierern wie _* far** und dem Qualifizierer **const** erstellt.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the \**\**_ designator, modifiers such as _\* far\*\*, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-135">*function-name*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-136">Gibt den Namen der Remoteprozedur an.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="bdbe9-137">*parameter-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="bdbe9-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbe9-138">Gibt null oder mehr richtungsale Attribute, Feldattribute, Verwendungsattribute und Zeigerattribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="bdbe9-139">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdbe9-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdbe9-140">Remarks</span></span>

<span data-ttu-id="bdbe9-141">MIT MIDL können Sie konstante integer-, character-, string- und boolean-Typen im Schnittstellentext der IDL-Datei deklarieren.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="bdbe9-142">**Const-Typdeklarationen** werden in der generierten Headerdatei als **\# define-Anweisungen** reproduziert.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="bdbe9-143">DCE-IDL-Compiler unterstützen keine konstanten Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="bdbe9-144">Daher ist dieses Feature nicht verfügbar, wenn Sie den MIDL-Compilerschalter [**/osf**](-osf.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="bdbe9-145">Eine zuvor definierte Konstante kann als zugewiesener Wert einer nachfolgenden Konstante verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="bdbe9-146">Der Wert eines konstanten integralen Ausdrucks wird gemäß C-Konvertierungsregeln automatisch in den entsprechenden ganzzahligen Typ konvertiert.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="bdbe9-147">Der Wert einer Zeichenkonstante muss ein ASCII-Zeichen mit einfachen Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="bdbe9-148">Wenn die Zeichenkonstante das einfache Anführungszeichen selbst (') ist, muss der umgekehrte Schrägstrich ( \\ ) dem einfachen Anführungszeichen voranstehen, wie in \\ .</span><span class="sxs-lookup"><span data-stu-id="bdbe9-148">When the character constant is the single-quote character itself ('), the backslash character (\\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="bdbe9-149">Der Wert einer Zeichenfolgenkonstante muss eine Zeichenfolge mit doppelten Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="bdbe9-150">Innerhalb einer Zeichenfolge muss der umgekehrte Schrägstrich ( **\\** ) einem literalen doppelten Anführungszeichen ( **"** ) vorangestellt werden, wie in **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="bdbe9-151">Innerhalb einer Zeichenfolge stellt der umgekehrte Schrägstrich ( **\\** ) ein Escapezeichen dar.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="bdbe9-152">Zeichenfolgenkonstanten können aus bis zu 255 Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="bdbe9-153">Der Wert **NULL** ist der einzige gültige Wert für Konstanten vom Typ [ \* *voidÂ \** _](void.md).</span><span class="sxs-lookup"><span data-stu-id="bdbe9-153">The value **NULL** is the only valid value for constants of type [\**voidÂ \** _](void.md).</span></span> <span data-ttu-id="bdbe9-154">Alle Attribute, die der \*_const\*\*-Deklaration zugeordnet sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-154">Any attributes associated with the _ *const*\* declaration are ignored.</span></span>

<span data-ttu-id="bdbe9-155">Der MIDL-Compiler überprüft bei der **const-Initialisierung** nicht auf Bereichsfehler.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="bdbe9-156">Wenn Sie beispielsweise "const short x = 0xFFFFFFFF;" angeben, meldet der MIDL-Compiler keinen Fehler, und der Initialisierer wird in der generierten Headerdatei reproduziert.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="bdbe9-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdbe9-157">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="bdbe9-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bdbe9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbe9-159">**Arrays**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-160">MIDL-Basistypen</span><span class="sxs-lookup"><span data-stu-id="bdbe9-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-162">**Byte**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-163">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-164">**Char**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-165">**\_Kontexthandle**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-166">**Enum**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-167">IDL-Datei (Interface Definition)</span><span class="sxs-lookup"><span data-stu-id="bdbe9-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-168">**Ignorieren**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-169">**lokal**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-170">**Lange**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-172">**Ptr**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-174">**short**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-175">**Unterzeichnet**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-176">**klein**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-177">**Schnur**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-178">**Struktur**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-179">**Union**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-180">**Einzigartige**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-181">**Unsigned**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-182">**void**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="bdbe9-183">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="bdbe9-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 