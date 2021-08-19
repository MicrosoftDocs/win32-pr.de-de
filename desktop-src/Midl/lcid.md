---
title: lcid-Attribut
description: Das \lcid\-Attribut gibt einen Gebietsschemabezeichner an und aktiviert gebietsschemaspezifische MIDL-Compilerunterstützung.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- LCID-Attribut MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87d1b6105d7e6ae561d7409cbf256b67f965c61e235ffc5782594cb5623497c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806796"
---
# <a name="lcid-attribute"></a>lcid-Attribut

Das **\[ \] lcid-Attribut** gibt einen Gebietsschemabezeichner an und ermöglicht gebietsschemaspezifische MIDL-Compilerunterstützung.

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Bibliothek**](library.md)an.

</dd> <dt>

*Localeid* 
</dt> <dd>

Gibt den 32-Bit-Gebietsschemabezeichner an, der in Windows National Language Support verwendet wird. In der Regel wird der Gebietsschemabezeichner hexadezimal angegeben.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Null oder mehr Attribute, die auf die [**Bibliothek**](library.md)angewendet werden sollen.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Name, mit dem Softwarekomponenten auf die [**Bibliothek**](library.md)verweisen.

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Eine oder mehrere MIDL-Anweisungen, die den Inhalt der [**Bibliothek**](library.md)definieren.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Null oder mehr MIDL-Attribute, die auf den Funktionsparameter angewendet werden.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt den Namen des Parameters in der IDL-Datei an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\[ \] lcid-Syntax** hat zwei verschiedene Formen: Die Auswirkung des Attributs hängt davon ab, welche Syntax Sie verwenden – entweder die Syntax der [**Bibliotheks-Anweisung**](library.md) oder die Parametersyntax.

Bei Anwendung [](library.md) auf die Bibliotheksanweisung zusammen mit einem localeID-Argument, wie im ersten Beispiel gezeigt, identifiziert das **\[ \] lcid-Attribut** das Gebietsschema für eine Typbibliothek oder für ein Funktionsargument und ermöglicht die Verwendung von internationalen Zeichen innerhalb des Bibliotheksblocks.

Ab Version 3.01.75 des MIDL-Compilers ist der von diesem Attribut bereitgestellte Gebietsschemabezeichner nicht nur mit der resultierenden Typbibliothek versehen, sondern ändert auch das Verhalten des Compilers. In [](library.md) einer Bibliotheksanweisung akzeptiert MIDL ab dem Punkt, an dem das **\[ \] lcid-Attribut** verwendet wird, eingaben, die gemäß dem angegebenen Gebietsschema lokalisiert sind. Insbesondere steht vollständige Unterstützung für asienische Sprachen wie Japanisch, Chinesisch und Koreanisch (vollständige DBCS-Unterstützung) zur Verfügung. Von der Lokalisierung unterstützte Features sind: Kommentare, Zeichenfolgen, HelpStrings und Bezeichner.

Verwenden Sie den Compilerschalter [**/lcid,**](-lcid.md) damit diese Lokalisierungsunterstützung für die gesamte Eingabedatei verfügbar ist, einschließlich Dateiname und Verzeichnispfad, anstatt nur innerhalb des Bibliotheksblocks.

Bei Anwendung auf einen Parameter können Sie mit dem **\[ \] lcid-Attribut** einen Gebietsschemabezeichner an eine Funktion übergeben, wie im zweiten Beispiel gezeigt. Die folgenden Einschränkungen gelten für **\[ \] lcid-Parameter:**

-   Eine Funktion kann höchstens einen **\[ lcid-Parameter \]** aufweisen.
-   Der Datentyp des Parameters muss [**long**](long.md)sein.
-   Die Richtung des Parameters darf nur **\[** [**in**](in.md) **\]** sein.
-   Der **\[ \] lcid-Parameter** muss allen anderen Parametern folgen, mit Ausnahme eines **\[** [**Retval-Parameters.**](retval.md) **\]**
-   Sie können das **\[ \] lcid-Attribut** nicht auf einen [**dispinterface-**](dispinterface.md) oder [**coclass-Parameter**](coclass.md) anwenden.

## <a name="examples"></a>Beispiele

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/lcid**](-lcid.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Retval**](retval.md)
</dt> </dl>

 

 