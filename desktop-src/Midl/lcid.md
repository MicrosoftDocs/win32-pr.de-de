---
title: LCID-Attribut
description: Das Attribut \ LCID \ gibt einen Gebiets Schema Bezeichner an und ermöglicht Gebiets Schema spezifische Unterstützung für den-Compiler.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- LCID-Attribut-Mittel l
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725096"
---
# <a name="lcid-attribute"></a>LCID-Attribut

Das **\[ LCID \]** -Attribut gibt einen Gebiets Schema Bezeichner an und ermöglicht Gebiets Schema spezifische Unterstützung für den Mittelwert Compiler.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die [**Bibliothek**](library.md)an.

</dd> <dt>

*LocaleID* 
</dt> <dd>

Gibt den 32-Bit-Gebiets Schema Bezeichner an, der in der Unterstützung von Windows- In der Regel wird der Gebiets Schema Bezeichner in hexadezimal angegeben.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

NULL oder mehr Attribute, die auf die [**Bibliothek**](library.md)angewendet werden sollen.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Name, mit dem Softwarekomponenten auf die [**Bibliothek**](library.md)verweisen.

</dd> <dt>

*Library-Definition-Anweisungen* 
</dt> <dd>

Eine oder mehrere-Mittell-Anweisungen, die den Inhalt der [**Bibliothek**](library.md)definieren.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

NULL oder mehr mittlere Attribute, die auf den Funktionsparameter angewendet werden.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Namen des Parameters in der IDL-Datei an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\[ LCID \]** -Syntax verfügt über zwei verschiedene Formen: die Auswirkung des Attributs hängt davon ab, welche Syntax Sie verwenden – entweder der Syntax der [**Bibliotheks**](library.md) Anweisung oder der Parameter Syntax.

Wenn das LCID-Attribut, wie im ersten Beispiel gezeigt, zusammen mit einem LocaleID-Argument auf die [**Library**](library.md) -Anweisung angewendet wird, identifiziert das **\[ LCID \]** -Attribut das Gebiets Schema für eine Typbibliothek oder für ein Funktions Argument und ermöglicht die Verwendung internationaler Zeichen innerhalb des Bibliotheks Blocks.

Mit der Version 3.01.75 des mittlerer l-Compilers wird der von diesem Attribut bereitgestellte Gebiets Schema Bezeichner nicht nur die resultierende Typbibliothek, sondern das Verhalten des Compilers geändert. Innerhalb einer [**Library**](library.md) -Anweisung akzeptiert die Mittel Stelle ab dem Zeitpunkt, an dem das **\[ LCID \]** -Attribut verwendet wird, die nach dem angegebenen Gebiets Schema lokalisierte Eingabe. Insbesondere ist eine vollständige Unterstützung für asiatische Sprachen wie Japanisch, Chinesisch und Koreanisch (vollständige DBCS-Unterstützung) verfügbar. Die von der Lokalisierung unterstützten Funktionen sind: Kommentare, Zeichen folgen, helpstrings und Bezeichner.

Verwenden Sie den [**/LCID**](-lcid.md) -Compilerschalter, um diese Lokalisierungsunterstützung für die gesamte Eingabedatei, einschließlich Dateiname und Verzeichnispfad, anstelle des Bibliotheks Blocks verfügbar zu lassen.

Wenn das **\[ LCID \]** -Attribut auf einen Parameter angewendet wird, können Sie einen Gebiets Schema Bezeichner an eine Funktion übergeben, wie im zweiten Beispiel dargestellt. Für **\[ LCID \]** -Parameter gelten die folgenden Einschränkungen:

-   Eine Funktion kann höchstens einen **\[ LCID \]** -Parameter aufweisen.
-   Der Datentyp des-Parameters muss [**lang**](long.md)sein.
-   Die Richtung des-Parameters darf **\[** nur [**in**](in.md) sein **\]** .
-   Der **\[ LCID \]** -Parameter muss mit Ausnahme eines **\[** [**retval**](retval.md) -Parameters allen anderen Parametern folgen **\]** .
-   Sie können das **\[ LCID \]** -Attribut nicht auf einen [**dispinterface**](dispinterface.md) -oder einen [**Co-Klasse**](coclass.md) -Parameter anwenden.

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

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/LCID**](-lcid.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 