---
description: Jedes Gebiets Schema hat einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einer Sprach-ID und einer Sortierreihenfolge-ID besteht.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Gebiets Schema Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339729"
---
# <a name="locale-identifiers"></a>Gebiets Schema Bezeichner

Jedes [Gebiets](locales-and-languages.md) Schema hat einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einer [sprach](language-identifiers.md) -ID und einer [Sortierreihenfolge](sort-order-identifiers.md)-ID besteht. Der Gebiets Schema Bezeichner ist eine standardmäßige internationale numerische Abkürzung und verfügt über die Komponenten, die zur eindeutigen Identifizierung eines der installierten, Betriebssystem definierten Gebiets Schemas erforderlich sind. NLS unterstützt sowohl vordefinierte Gebiets Schema Bezeichner als auch benutzerdefinierte Bezeichner.

> [!Note]  
> Gebiets Schema Namen können mit in Windows Vista eingeführten Funktionen verwendet werden, die anstelle eines Gebiets Schema Bezeichners einen Gebiets Schema [Namen](locale-names.md) als Parameter annehmen. Weitere Informationen finden Sie unter [Aufrufen der "locale Name"-Funktionen](calling-the--locale-name--functions.md). Die Verwendung von Gebiets Schema Namen anstelle von Gebiets Schema bezeichnermerkmalen ist immer vorzuziehen.

 

Die folgende Abbildung zeigt das Format der Bits in einem Gebiets Schema Bezeichner.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Vordefinierte Gebiets Schema Bezeichner

Die von NLS unterstützten vordefinierten Gebiets Schema Bezeichner sind in der API-Referenz für die [National Language Support (NLS)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)definiert.

NLS verwendet die folgenden Gebiets Schema Informations Konstanten zur Darstellung von Gebiets Schema Bezeichners.

-   Gebiets Schema [ \_ SLanguage](locale-slanguage.md) oder [locale \_ slocalizedlanguagename](locale-slocalized-constants.md)
-   [Name des Gebiets Schemas \_](locale-sname.md)
-   [Gebiets Schema- \_ sscripts](locale-sscripts.md)
-   [Gebiets Schema \_ idefaultansicodepage](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Benutzerdefinierte Gebiets Schema Bezeichner

**Windows Vista:** NLS unterstützt die benutzerdefinierten Gebiets Schema Bezeichner, die durch die folgenden Gebiets Schema Informations Konstanten dargestellt werden.

-   [\_benutzerdefinierter locale- \_ Standard](locale-custom-constants.md)
-   [benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung](locale-custom-constants.md)
-   [Gebiets Schema \_ Benutzer \_ definiert nicht angegeben](locale-custom-constants.md)

## <a name="building-a-locale"></a>Aufbauen eines Gebiets Schemas

Zum Erstellen von Gebiets Schemas können Sie das von NLS bereitgestellte Hilfsprogramm "Locale Builder" verwenden. Weitere Informationen finden Sie unter [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).

Die Anwendung kann einen Gebiets Schema Bezeichner mit dem [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro erstellen. Alternativ kann Sie einen der Standard Bezeichner verwenden, die den unten aufgeführten Konstanten entsprechen.

-   [Gebiets Schema \_ invariant](locale-invariant.md)
-   [Standard für Gebiets Schema \_ System \_](locale-system-default.md)
-   [\_Standardbenutzer Name für locale \_](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Abrufen von Gebiets Schema Bezeichnerzeichen

Eine Anwendung kann die aktuellen Gebiets Schema Bezeichner mithilfe der Funktionen [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) und [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) abrufen. Jeder Thread kann sein eigenes Gebiets Schema mit [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) und [**getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)festlegen und abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Sprachen-IDs](language-identifiers.md)
</dt> <dt>

[Gebiets Schema Namen](locale-names.md)
</dt> <dt>

[Sortierreihenfolge-IDs](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
