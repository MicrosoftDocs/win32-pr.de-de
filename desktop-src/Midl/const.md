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
# <a name="const-attribute"></a>Konstanten Attribut

Das Schlüsselwort " **Konstanten** " ändert den Typ einer Typdeklaration oder den Typ eines Funktions Parameters, wodurch der Wert nicht unterschiedlich ist.

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

*"Typ"-Typ* 
</dt> <dd>

Gibt eine gültige Zeichenfolge, ein Zeichen, eine Zeichenfolge oder einen booleschen Wert für die mittlere Zahl an. Zu den gültigen Mittel Typen zählen [**Small**](small.md), [**Short**](short.md), [**Long**](long.md) [](char-idl.md) [](byte.md) **\***, Char, Char, [**WCHAR \_**](wchar-t.md) **\_ \*** **\*** t, [**\***](void.md)WCHAR t, Byte, Byteund void. Die ganzzahligen und Zeichen Typen können mit oder [**ohne**](unsigned.md)Vorzeichen [**signiert**](signed.md) werden.

</dd> <dt>

*identifier* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> <dt>

*Ausdruck "Konstanten"* 
</dt> <dd>

Gibt einen Ausdruck, einen Bezeichner oder eine numerische oder Zeichen Konstante für den angegebenen Typ an: Konstante ganzzahlige Literale oder Konstante ganzzahlige Ausdrücke für ganzzahlige Konstanten. Boolesche Ausdrücke, die bei der Kompilierung für [**boolesche**](boolean.md) Typen berechnet werden können. Einzelzeichen Konstanten für [**char**](char-idl.md) -Typen; und Zeichen folgen Konstanten für **\[** [**Zeichen**](string.md) folgen **\]** Typen. Der Typ [**"void" \***](void.md) kann nur mit **null** initialisiert werden.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.

</dd> <dt>

*Zeigertyp* 
</dt> <dd>

Gibt einen gültigen Mittell-Zeigertyp an.

</dd> <dt>

*Deklarator und Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.

</dd> <dt>

*Function-attr-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn **\*** Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " **Konstanten**" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mithilfe von "Mittel l" können Sie Konstante Integer-, Zeichen-, Zeichen folgen-und boolesche Typen im Schnittstellen Text der IDL-Datei deklarieren. Die **Konstanten** Typdeklarationen werden in der generierten Header Datei als **\# define** -Direktiven reproduziert.

DCE-IDL-Compiler unterstützen keine Konstanten Ausdrücke. Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.

Eine zuvor definierte Konstante kann als zugewiesener Wert einer nachfolgenden Konstante verwendet werden. Der Wert eines Konstanten ganzzahligen Ausdrucks wird in Übereinstimmung mit C-Konvertierungsregeln automatisch in den entsprechenden ganzzahligen Typ konvertiert.

Der Wert einer Zeichen Konstante muss ein ASCII-Zeichen mit nur einem Anführungszeichen sein. Wenn die Zeichen Konstante das einfache Anführungszeichen (') ist, muss der umgekehrte Schrägstrich ( \) wie in ' ' vor dem einfachen Anführungszeichen stehen \\ .

Der Wert einer Zeichen folgen Konstante muss eine Zeichenfolge in doppelten Anführungszeichen sein. Innerhalb einer Zeichenfolge muss der umgekehrte Schrägstrich ( **\\** ) dem literalen doppelten Anführungszeichen ( **"** ) vorangestellt werden, wie in **\\ "**. Innerhalb einer Zeichenfolge stellt der umgekehrte Schrägstrich ( **\\** ) ein Escapezeichen dar. Zeichen folgen Konstanten können bis zu 255 Zeichen umfassen.

Der Wert **null** ist der einzige gültige Wert für Konstanten vom Typ [**"void" \***](void.md). Alle Attribute, die der **Konstanten** Deklaration zugeordnet sind, werden ignoriert.

Der mittlerer l-Compiler überprüft bei der **Konstanten** Initialisierung keine Bereichs Fehler. Wenn Sie z. b. "Konstante Short x = 0xffffffff;" angeben, meldet der Mittell-Compiler keinen Fehler, und der Initialisierer wird in der generierten Header Datei reproduziert.

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

[**Mikro**](arrays-1.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Booleschen**](boolean.md)
</dt> <dt>

[**Hobby**](byte.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 