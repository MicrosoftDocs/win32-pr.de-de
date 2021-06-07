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
# <a name="const-attribute"></a>const-Attribut

Das **schlüsselwort const** ändert den Typ einer Typdeklaration oder den Typ eines Funktionsparameters, sodass der Wert nicht variiert.

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*const-type* 
</dt> <dd>

Gibt eine gültige MIDL-Ganzzahl, ein gültiges Zeichen, eine Zeichenfolge oder einen booleschen Typ an. Gültige MIDL-Typen sind [**kleine**](small.md), [**kurze**](short.md), [**lange**](long.md), [**char**](char-idl.md), **\* charÂ* _, _ [*wchar \_ t* *](wchar-t.md), **wchar \_ \* tÂ*_, _ [*byte* *](byte.md), **byteÂ \** _, und [_*void". \**_](void.md) Die Ganzzahl- und Zeichentypen können [*_signed* *](signed.md) oder [**unsigned**](unsigned.md)sein.

</dd> <dt>

*identifier* 
</dt> <dd>

Gibt einen gültigen MIDL-Bezeichner an. Gültige MIDL-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder Unterstrichen und müssen mit einem Alphabet- oder Unterstrich beginnen.

</dd> <dt>

*const-expression* 
</dt> <dd>

Gibt einen Ausdruck, einen Bezeichner oder eine numerische oder Zeichenkonstante an, die für den angegebenen Typ geeignet ist: konstante ganzzahlige Literale oder konstante ganzzahlige Ausdrücke für ganzzahlige Konstanten; Boolesche Ausdrücke, die bei der Kompilierung für [**boolesche**](boolean.md) Typen berechnet werden können. Einzelzeichenkonstanten [](char-idl.md) für Char-Typen; und Zeichenfolgenkonstanten für **\[** [](string.md) **\]** Zeichenfolgentypen. Der [ * *voidÂ \** _-Typ](void.md) kann nur mit _*NULL** initialisiert werden.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten.

</dd> <dt>

*Zeigertyp* 
</dt> <dd>

Gibt einen gültigen MIDL-Zeigertyp an.

</dd> <dt>

*deklarator und declarator-list* 
</dt> <dd>

Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Die *Deklaratorliste* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameternamenbezeichner im Funktionsdeklarator ist optional.

</dd> <dt>

*function-attr-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[** [**rückruf,**](callback.md) **\]** **\[** [**local,**](local.md) **\]** das Zeigerattribut **\[** [**ref,**](ref.md) **\]** **\[** [**eindeutig**](unique.md)oder **\]** **\[** [**ptr**](ptr.md)und die **\]** Verwendungsattribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**\_ Kontexthandle**](context-handle.md) **\]** .

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp,](midl-base-types.md) [**eine Struktur,**](struct.md) [**einen Union-,**](union.md) [**Enumerations-**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator ist identisch mit dem in C verwendeten Zeigerdeklarator. Sie wird aus dem **\* *_-Bezeichner, Modifizierern wie _* far** und dem Qualifizierer **const** erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Gibt null oder mehr richtungsale Attribute, Feldattribute, Verwendungsattribute und Zeigerattribute an, die für den angegebenen Parametertyp geeignet sind. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

MIT MIDL können Sie konstante integer-, character-, string- und boolean-Typen im Schnittstellentext der IDL-Datei deklarieren. **Const-Typdeklarationen** werden in der generierten Headerdatei als **\# define-Anweisungen** reproduziert.

DCE-IDL-Compiler unterstützen keine konstanten Ausdrücke. Daher ist dieses Feature nicht verfügbar, wenn Sie den MIDL-Compilerschalter [**/osf**](-osf.md) verwenden.

Eine zuvor definierte Konstante kann als zugewiesener Wert einer nachfolgenden Konstante verwendet werden. Der Wert eines konstanten integralen Ausdrucks wird gemäß C-Konvertierungsregeln automatisch in den entsprechenden ganzzahligen Typ konvertiert.

Der Wert einer Zeichenkonstante muss ein ASCII-Zeichen mit einfachen Anführungszeichen sein. Wenn die Zeichenkonstante das einfache Anführungszeichen selbst (') ist, muss der umgekehrte Schrägstrich ( \\ ) dem einfachen Anführungszeichen voranstehen, wie in \\ .

Der Wert einer Zeichenfolgenkonstante muss eine Zeichenfolge mit doppelten Anführungszeichen sein. Innerhalb einer Zeichenfolge muss der umgekehrte Schrägstrich ( **\\** ) einem literalen doppelten Anführungszeichen ( **"** ) vorangestellt werden, wie in **\\ "**. Innerhalb einer Zeichenfolge stellt der umgekehrte Schrägstrich ( **\\** ) ein Escapezeichen dar. Zeichenfolgenkonstanten können aus bis zu 255 Zeichen bestehen.

Der Wert **NULL** ist der einzige gültige Wert für Konstanten vom Typ [ * *voidÂ \** _](void.md). Alle Attribute, die der *_const**-Deklaration zugeordnet sind, werden ignoriert.

Der MIDL-Compiler überprüft bei der **const-Initialisierung** nicht auf Bereichsfehler. Wenn Sie beispielsweise "const short x = 0xFFFFFFFF;" angeben, meldet der MIDL-Compiler keinen Fehler, und der Initialisierer wird in der generierten Headerdatei reproduziert.

## <a name="examples"></a>Beispiele

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

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**Byte**](byte.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**Lange**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Unterzeichnet**](signed.md)
</dt> <dt>

[**klein**](small.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 