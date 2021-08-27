---
title: Bibliothekattribut
description: Die Library-Anweisung enthält alle Informationen, die der MIDL-Compiler zum Generieren einer Typbibliothek verwendet.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- Bibliotheksattribut MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086370"
---
# <a name="library-attribute"></a>Bibliothekattribut

Die **Library-Anweisung** enthält alle Informationen, die der MIDL-Compiler zum Generieren einer Typbibliothek verwendet.

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

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die Bibliothek an.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt zusätzliche Attribute an, die für die gesamte **Bibliotheks-Anweisung gelten.** Zulässige Attribute sind **\[** [**Steuerelement,**](control.md) **\]** **\[** [**HelpContext,**](helpcontext.md) **\]** **\[** [**Helpfile,**](helpfile.md) **\]** **\[** [**HelpString,**](helpstring.md) **\]** **\[** [**ausgeblendet,**](hidden.md) **\]** **\[** [**lcid,**](lcid.md)eingeschränkt **\]** **\[** [**und**](restricted.md) **\]** **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Name, mit dem Softwarekomponenten auf die Bibliothek **verweisen.**

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Eine oder mehrere MIDL-Anweisungen, die den Inhalt der Bibliothek **definieren.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Anweisungen innerhalb des Bibliotheksblocks können Elemente verwenden, die innerhalb oder außerhalb des Bibliotheksblocks deklariert werden. Bibliotheksanweisungen können diese Elemente als Basistypen verwenden, von diesen Elementen erben oder einfach wie folgt in einer Zeile darauf verweisen:

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

Der MIDL-Compiler erstellt eine Typbibliothek, die Definitionen für jedes Element innerhalb des Bibliotheksblocks sowie Definitionen für alle Elemente enthält, die außerhalb des Bibliotheksblocks definiert sind und auf die innerhalb des Bibliotheksblocks verwiesen wird.

Informationen zum Generieren einer Typbibliothek sowie von Proxystubs und Headern aus einer einzelnen IDL-Datei finden Sie unter Generieren einer Proxy-DLL und einer Typbibliothek aus einer einzelnen [IDL-Datei.](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md)

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

[**Steuerung**](control.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Versteckte**](hidden.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Beschränkt**](restricted.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 