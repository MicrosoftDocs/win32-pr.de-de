---
title: Bibliotheks Attribut
description: Die Library-Anweisung enthält alle Informationen, die vom-Mittelwert Compiler zum Generieren einer Typbibliothek verwendet werden.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- Bibliotheks Attribut-Mittel l
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338659"
---
# <a name="library-attribute"></a>Bibliotheks Attribut

Die **Library** -Anweisung enthält alle Informationen, die vom-Mittelwert Compiler zum Generieren einer Typbibliothek verwendet werden.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die Bibliothek an.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt zusätzliche Attribute an, die auf die gesamte **Bibliotheks** Anweisung angewendet werden. Zulässige Attribute sind **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**restricted**](restricted.md) **\]** und **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Name, mit dem Softwarekomponenten auf die **Bibliothek** verweisen.

</dd> <dt>

*Library-Definition-Anweisungen* 
</dt> <dd>

Eine oder mehrere-Mittell-Anweisungen, die den Inhalt der **Bibliothek** definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

-Anweisungen innerhalb des Bibliotheks Blocks können Elemente verwenden, die innerhalb oder außerhalb des Bibliotheks Blocks deklariert werden. Bibliotheks Anweisungen können diese Elemente als Basis Typen verwenden, von diesen Elementen erben oder einfach in einer Zeile auf Sie verweisen, wie im folgenden dargestellt:

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

Der mittlerer l-Compiler erstellt eine Typbibliothek, die Definitionen für jedes Element innerhalb des Bibliotheks Blocks sowie Definitionen für alle Elemente enthält, die außerhalb des Bibliotheks Blocks definiert sind und auf die verwiesen wird.

Informationen zum Erstellen eines Typbibliothek-und proxystubys und von Headern aus einer einzelnen IDL-Datei finden Sie unter [Erstellen einer Proxy-dll und einer Typbibliothek aus einer einzelnen IDL-Datei](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inhalt einer Typbibliothek](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Steuerelement**](control.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**verbirgt**](hidden.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**begrenz**](restricted.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 