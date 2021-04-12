---
description: In diesem Thema wird beschrieben, wie Sie in Ihren Anwendungen mit internationalisierten Domänen Namen (Internationalized Domain Names, IDNs) arbeiten.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Umgang mit internationalisierten Domänen Namen (IDNs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216947"
---
# <a name="handling-internationalized-domain-names-idns"></a>Umgang mit internationalisierten Domänen Namen (IDNs)

In diesem Thema wird beschrieben, wie Sie in Ihren Anwendungen mit internationalisierten Domänen Namen (Internationalized Domain Names, IDNs) arbeiten. IDNs werden von der Netzwerk Arbeitsgruppe [RFC 3490: internationalisieren von Domänen Namen in Anwendungen (IDNA)](http://www.faqs.org/rfcs/rfc3490.html)angegeben. Vor diesem Entwurfs Standard waren IDNs auf lateinische Zeichen ohne Diakritik beschränkt. IDNA ermöglicht IDNs das Einschließen von lateinischen Zeichen mit Diakritik und Zeichen aus nicht lateinischen Skripts, wie z. b. Kyrillisch, Arabisch und Chinesisch. Der Standard definiert auch Regeln für die Zuordnung von IDNs zu reinen ASCII-Domänen Namen. Daher können IDNA-Probleme auf Clientseite behandelt werden, ohne dass DNS (Domain Nameserver)-Änderungen erforderlich sind.

> [!Caution]  
> In RFC 3490 wird eine Reihe von Sicherheitsproblemen im Zusammenhang mit der Verwendung von IDNs eingeführt. Weitere Informationen finden Sie im entsprechenden Abschnitt der [Sicherheitsaspekte: Internationale Features](security-considerations--international-features.md).

 

> [!Note]  
> IDNA basiert derzeit auf Unicode 3,2.

 

## <a name="nls-api-functions-for-handling-idns"></a>NLS API Funktionen für die Handhabung von IDNs

NLS umfasst die folgenden Konvertierungs Funktionen, die Ihre Anwendung verwenden kann, um einen IDN in verschiedene Darstellungen zu konvertieren. Ein Beispiel für die Verwendung dieser Funktionen finden Sie unter [nls: Beispiel für die Konvertierung von internationalisierten Domänen Namen (IDN)](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**Idnto ASCII**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Konvertiert einen IDN in Punycode.
-   [**Idntonameprepunicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Führt den Nameprep-Teil der Konvertierung eines IDN in einen ASCII-Namen aus. Diese Funktion erstellt eine kanonische Unicode-Darstellung einer Zeichenfolge.
-   [**Idnzu Unicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Konvertiert eine Punycode-Zeichenfolge in eine normale UTF-16-Zeichenfolge.

NLS definiert auch mehrere API-Funktionen, die verwendet werden können, um einige der von der IDN-Technologie dargestellten Sicherheitsrisiken zu entschärfen. Unter Windows Vista und höher werden die folgenden Funktionen verwendet, um zu überprüfen, ob die Zeichen in einem angegebenen IDN vollständig aus den Skripts gezeichnet werden, die einem bestimmten Gebiets Schema oder Gebiets Schema zugeordnet sind. Ein Beispiel für die Verwendung dieser Funktionen finden Sie unter [nls: Beispiel zur Entschärfung der internationalisierten Domänen Namen (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**Getstringscripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Stellt eine Liste der in einer bestimmten Zeichenfolge verwendeten Skripts bereit.
-   [**Getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**getlocaleingefoex**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Abrufen von Gebiets Schema Informationen. Die Verwendung der Funktionen, bei denen *LCTYPE* auf [locale \_ sscripts](locale-sscripts.md) festgelegt ist, enthält eine Liste von Skripts, die normalerweise für ein bestimmtes Gebiets Schema
-   [**Verifyscripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Vergleicht die Liste der Skripts. Zum Überprüfen mehrerer Gebiets Schemas kann die Anwendung mehrere Aufrufe an [**getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**getlocaleingefoex**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) und [**verifyscripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)durchführen.

Bei Anwendungen, die unter Windows XP und Windows Server 2003 ausgeführt werden, spielen die Funktionen " [**downlevelgetlocalescripts**](downlevelgetlocalescripts.md)", " [**downlevelgetstringscripts**](downlevelgetstringscripts.md)" und " [**downlevelverifyscripts**](downlevelverifyscripts.md) " eine ähnliche Rolle wie bei den oben aufgeführten Funktionen, um das Sicherheitsrisiko zu mindern. Der Download ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) ist im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar.

## <a name="handle-unicode-strings"></a>Unicode-Zeichen folgen verarbeiten

IDNA unterstützt die Transformation von Unicode-Zeichen folgen in legitime hostnamensbezeichnungen, mit Ausnahme von Zeichen folgen, die bestimmte unzulässige Zeichen enthalten, z. b. Steuerzeichen, Zeichen aus dem privaten Verwendungsbereich (Pua) und ähnliches. Die Anwendung kann das IDN \_ use \_ STD3 \_ ASCII Rules- \_ Flag mit mehreren nls-Konvertierungs Funktionen verwenden, um zu erzwingen, dass die Funktionen fehlschlagen, wenn Sie andere ASCII-Zeichen als Buchstaben, Ziffern oder Bindestriche-Minuszeichen (-) aufweisen oder wenn eine Zeichenfolge mit dem Bindestrich-Minuszeichen beginnt oder endet. Diese Zeichen sind für die Verwendung in Domänen Namen immer unzulässig und bleiben im Entwurfs Standard unverändert.

## <a name="handle-unassigned-code-points"></a>Nicht zugewiesene Code Punkte behandeln

IDNs können nicht zugewiesene Code Punkte enthalten. Daher verfügen Code Punkte, die nicht mit einem Zeichen ("zugewiesen") ab dem Unicode 3,2 zugeordnet sind, nicht über definierte IDN-Zuordnungen, obwohl das IDN- \_ \_ Flag "nicht zugewiesen" in bestimmten Konvertierungs Funktionen zulässt, dass Sie Punycode zugeordnet werden können. Eine Liste nicht zugewiesener Code Punkte finden Sie in [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Wenn Ihre Anwendung nicht zugewiesene Code Punkte als Punycode codiert, sollten die resultierenden Domänen Namen ungültig sein. Die Sicherheit kann beeinträchtigt werden, wenn diese Namen in einer neueren Version von IDNA zulässig sind oder wenn die Anwendung die ungültigen Zeichen herausfiltert, um einen rechtlichen Domänen Namen zu erstellen.

 

Nicht zugewiesene Code Punkte sind in den gespeicherten Zeichen folgen, die in Protokoll bezeichnerelementen und benannten Entitäten verwendet werden, nicht zulässig, wie z. b. Namen in digitalen Zertifikaten und DNS-Domänen Namen. Die Code Punkte sind jedoch in Abfrage Zeichenfolgen zulässig, z. b. Benutzernamen für digitale Zertifizierungsstellen und DNS-Lookups, die für den Abgleich mit gespeicherten bezeichnervorgängen verwendet werden.

> [!Caution]  
> Obwohl für Abfrage Zeichenfolgen nicht zugewiesene Code Punkte verwendet werden können, sollten Sie in Ihren Anwendungen nicht verwendet werden. Selbst eine vom Benutzer bereitgestellte Abfrage Zeichenfolge stellt das Risiko eines "Spoofing"-Angriffs dar. Bei dieser Art von Angriff führt die skrupellose Host Website Benutzer von der Website, auf die Sie zugreifen möchten, erneut aus, um Sie auf eine andere Site zuzugreifen, die möglicherweise vertrauliche Informationen für einen Drittanbieter bereitstellt. Beispielsweise kann das Kopieren einer Zeichenfolge aus einer eingehenden e-Mail dieselben Risiken wie das Klicken auf einen Link in einem Browser darstellen.

 

## <a name="convert-domain-names-to-ascii-names"></a>Konvertieren von Domänen Namen in ASCII-Namen

Die Anwendung kann die [**idntoascii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) -Funktion und bestimmte Entschärfungs Funktionen verwenden, um IDNs in ASCII zu konvertieren.

> [!Caution]  
> Da Zeichen folgen mit sehr unterschiedlichen binären Darstellungen als identisch verglichen werden können, kann diese Funktion bestimmte Sicherheitsprobleme lösen. Weitere Informationen finden Sie in der Erörterung der Vergleichsfunktionen in [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="examples"></a>Beispiele

NLS: Beispiel für die IDN-Konvertierung [(Internationalized Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md) veranschaulicht die Verwendung der IDN-Konvertierungs Funktionen. [Nls: Internationalized Domain Name (IDN) Entschärfungs Beispiel](nls--internationalized-domain-name--idn--mitigation-sample.md) veranschaulicht die Verwendung der IDN-Entschärfungs Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Überlegungen zur Sicherheit: Internationale Features](security-considerations--international-features.md)
</dt> </dl>

 

 



