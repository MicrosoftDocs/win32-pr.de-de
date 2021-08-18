---
description: In diesem Thema wird beschrieben, wie Sie mit internationalisierten Domänennamen (IDNs) in Ihren Anwendungen arbeiten können.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Behandeln von internationalisierten Domänennamen (IDNs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310cf74e39758dc6974a1247fe9a5b506276f5c3da55d546d6bc6c2b5a8c992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898584"
---
# <a name="handling-internationalized-domain-names-idns"></a>Behandeln von internationalisierten Domänennamen (IDNs)

In diesem Thema wird beschrieben, wie Sie mit internationalisierten Domänennamen (IDNs) in Ihren Anwendungen arbeiten können. IDNs werden von der Netzwerkarbeitsgruppe [RFC 3490: Internationalizing Domain Names in Applications (IDNA) angegeben.](http://www.faqs.org/rfcs/rfc3490.html) Vor diesem Standardentwurf waren IDNs auf lateinische Zeichen ohne diakritische Zeichen beschränkt. MIT IDNA können IDNs lateinische Zeichen mit diakritischen Zeichen sowie Zeichen aus nicht lateinischen Skripts wie Kyrillisch, Arabisch und Chinesisch enthalten. Der Standard legt auch Regeln für die Zuordnung von IDNs zu ausschließlich ASCII-Domänennamen fest. Daher können IDNA-Probleme auf clientseitiger Seite behandelt werden, ohne dass Dns-Änderungen (Domain Name Server) erforderlich sind.

> [!Caution]  
> RFC 3490 führt eine Reihe von Sicherheitsproblemen im Zusammenhang mit der Verwendung von IDNs ein. Weitere Informationen finden Sie im entsprechenden Abschnitt zu [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

> [!Note]  
> IDNA basiert derzeit auf Unicode 3.2.

 

## <a name="nls-api-functions-for-handling-idns"></a>NLS API-Funktionen für die Behandlung von IDNs

NLS enthält die folgenden Konvertierungsfunktionen, mit denen Ihre Anwendung einen IDN in verschiedene Darstellungen konvertieren kann. Ein Beispiel für die Verwendung dieser Funktionen finden Sie unter [NLS: Internationalized Domain Name (IDN) Conversion Sample (NLS: IDN-Konvertierungsbeispiel).](nls--internationalized-domain-name--idn--conversion-sample.md)

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Konvertiert einen IDN in Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Führt den NamePrep-Teil der Konvertierung eines IDN in einen ASCII-Namen aus. Diese Funktion erstellt eine kanonische Unicode-Darstellung einer Zeichenfolge.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Konvertiert eine Punycode-Zeichenfolge in eine normale UTF-16-Zeichenfolge.

NLS definiert auch mehrere API-Funktionen, die verwendet werden können, um einige der Sicherheitsrisiken zu minimieren, die durch die IDN-Technologie verbunden sind. Unter Windows Vista und höher werden die folgenden Funktionen verwendet, um sicherzustellen, dass die Zeichen in einem bestimmten IDN vollständig aus den Skripts gezeichnet werden, die einem bestimmten Oder einem bestimmten Locale zugeordnet sind. Ein Beispiel für die Verwendung dieser Funktionen finden Sie unter NLS: IdN-Entschärfungsbeispiel [(NLS: Internationalized Domain Name, internationalisierter Domänenname).](nls--internationalized-domain-name--idn--mitigation-sample.md)

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Stellt eine Liste der Skripts zur Verfügung, die in einer bestimmten Zeichenfolge verwendet werden.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Abrufen von Locale-Informationen. Die Verwendung der Funktionen mit *LCType,* die [auf LOCALE \_ SSCRIPTS festgelegt sind,](locale-sscripts.md) stellt eine Liste von Skripts zur Verfügung, die normalerweise für ein bestimmtes Locale verwendet werden.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Vergleicht Skriptlisten. Zur Überprüfung mit mehreren Lokalen kann die Anwendung mehrere Aufrufe von [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) und [**VerifyScripts tätigen.**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)

Für Anwendungen, die unter Windows XP und Windows Server 2003 ausgeführt werden, spielen die Funktionen [**DownlevelGetLocaleScripts,**](downlevelgetlocalescripts.md) [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)und [**DownlevelVerifyScripts**](downlevelverifyscripts.md) eine ähnliche Rolle wie die oben aufgeführten Funktionen zur Minderung des Sicherheitsrisikos. Der [Download "Microsoft Internationalized Domain Name (IDN)-Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) steht im [MSDN Download Center zur Verfügung.](https://www.microsoft.com/?ref=go)

## <a name="handle-unicode-strings"></a>Verarbeiten von Unicode-Zeichenfolgen

IDNA unterstützt die Transformation von Unicode-Zeichenfolgen in legitime Hostnamensbezeichnungen, mit Ausnahme von Zeichenfolgen, die bestimmte unzulässige Zeichen enthalten, z. B. Steuerzeichen, Zeichen aus dem privaten Verwendungsbereich (PUA) und deren Namen. Ihre Anwendung kann das IDN USE STD3 ASCII RULES-Flag mit mehreren \_ \_ \_ NLS-Konvertierungsfunktionen verwenden, um zu erzwingen, dass die Funktionen fehlschlagen, wenn andere ASCII-Zeichen als Buchstaben, Zahlen oder bindestriche-minus (-) Zeichen auftreten oder wenn eine Zeichenfolge mit dem Bindestrich minus beginnt oder \_ endet. Diese Zeichen wurden immer nicht in Domänennamen verwendet und bleiben im Entwurfsstandard nicht zulässig.

## <a name="handle-unassigned-code-points"></a>Behandeln von nicht zugewiesenen Codepunkten

IDNs dürfen keine nicht zugewiesenen Codepunkte enthalten. Daher verfügen Codepunkte, die ab Unicode 3.2 nicht einem Zeichen zugeordnet sind ("zugewiesen"), über keine definierten IDN-Zuordnungen, obwohl das IDN-Flag ALLOW UNASSIGNED in bestimmten Konvertierungsfunktionen die Zuordnung zu \_ \_ Punycode ermöglicht. Eine Liste der nicht zugewiesenen Codepunkte finden Sie in [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Wenn Ihre Anwendung nicht zugewiesene Codepunkte als Punycode codiert, sollten die resultierenden Domänennamen ungültig sein. Die Sicherheit kann beeinträchtigt werden, wenn diese Namen in einer späteren Version von IDNA legal sind oder wenn die Anwendung die unzulässigen Zeichen herausfiltert, um zu versuchen, einen rechtlichen Domänennamen zu erstellen.

 

Nicht zugewiesene Codepunkte sind in den gespeicherten Zeichenfolgen, die in Protokollbezeichnern und benannten Entitäten verwendet werden, nicht zulässig, z. B. Namen in digitalen Zertifikaten und DNS-Domänennamenteilen. Die Codepunkte sind jedoch in Abfragezeichenfolgen zulässig, z. B. vom Benutzer eingegebene Namen für digitale Zertifizierungsstellen und DNS-Suchabfragen, die für die Übereinstimmung mit gespeicherten Bezeichnern verwendet werden.

> [!Caution]  
> Obwohl Abfragezeichenfolgen nicht zugewiesene Codepunkte verwenden können, sollten Sie sie nicht in Ihren Anwendungen verwenden. Selbst eine vom Benutzer bereitgestellte Abfragezeichenfolge birgt das Risiko eines Spoofingangriffs. Bei dieser Art von Angriff werden Benutzer von der skrupellosen Hostwebsite von der Website umgeleitet, auf die sie zugreifen möchten, um auf eine andere Website zu zugreifen, die möglicherweise vertrauliche Informationen an einen Drittanbieter weiterleiten. Beispielsweise kann das Kopieren einer Zeichenfolge aus einer eingehenden E-Mail das gleiche Risiko mit sich wie das Klicken auf einen Link in einem Browser haben.

 

## <a name="convert-domain-names-to-ascii-names"></a>Konvertieren von Domänennamen in ASCII-Namen

Ihre Anwendung kann die [**IdnToAscii-Funktion**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) und bestimmte Entschärfungsfunktionen verwenden, um IDNs in ASCII zu konvertieren.

> [!Caution]  
> Da Zeichenfolgen mit sehr unterschiedlichen binären Darstellungen als identisch verglichen werden können, kann diese Funktion bestimmte Sicherheitsbedenken nach sich ziehen. Weitere Informationen finden Sie in der Diskussion zu Vergleichsfunktionen unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="examples"></a>Beispiele

[NLS: Das Konvertierungsbeispiel für internationalisierte Domänennamen (INTERNATIONALIZED Domain Name, IDN)](nls--internationalized-domain-name--idn--conversion-sample.md) veranschaulicht die Verwendung der IDN-Konvertierungsfunktionen. [NLS: Entschärfungsbeispiel für internationalisierte Domänennamen (INTERNATIONALIZED Domain Name, IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md) veranschaulicht die Verwendung der IDN-Entschärfungsfunktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung der Landessprache](using-national-language-support.md)
</dt> <dt>

[Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md)
</dt> </dl>

 

 



