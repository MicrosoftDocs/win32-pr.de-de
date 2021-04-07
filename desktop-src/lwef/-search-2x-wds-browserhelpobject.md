---
title: Aufrufen von WDS von Webseiten
description: Sie können Microsoft Windows Desktop Search (WDS) von jeder beliebigen Webseite, die Sie erstellen oder verwalten, mit dem Browserhilfsobjekt (BHO) und Windows Internet Explorer abrufen.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "104038662"
---
# <a name="calling-wds-from-web-pages"></a>Aufrufen von WDS von Webseiten

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Sie können Microsoft Windows Desktop Search (WDS) von jeder beliebigen Webseite, die Sie erstellen oder verwalten, mit dem Browserhilfsobjekt (BHO) und Windows Internet Explorer abrufen. Sie können sehen, wie dies auf der MSN-Webseite funktioniert. Über dem Suchfeld für https://www.msn.com gibt es mehrere Suchtypen: Web, News, Bilder, Desktop, Encarta und local. Wenn Sie auf Desktop klicken, werden die Suchparameter an die Windows-Desktop Suche übermittelt, die den Katalog durchsucht und Ergebnisse in der WDS-Benutzeroberfläche anzeigt. Damit Benutzer eine Desktop Suche von ihren Webseiten aus starten können, muss wdsbho auf Ihren Systemen installiert und aktiviert sein. Ihre Webseiten müssen als zulässige URL bei WDS registriert sein, und Sie müssen einen Link erstellen, um die vom Benutzer getaktete Abfrage an WDS zu übergeben.

## <a name="enabling-the-wds-browser-help-object"></a>Aktivieren des Hilfe Objekts für den WDS-Browser

Der BHO wird bei der Installation von WDS standardmäßig in Internet Explorer installiert und aktiviert, aber Sie können problemlos überprüfen, ob er deaktiviert oder deinstalliert wurde. Öffnen Sie im System eines Benutzers Internet Explorer, wählen Sie **im Menü Extras die** **Option Internetoptionen** aus, klicken Sie auf die Registerkarte **Programme** , und klicken Sie dann auf **Add-ons verwalten**. Suchen Sie in der Liste der Add-ons nach der Klasse dsweballowbho, und stellen Sie sicher, dass Sie aktiviert ist. Wenn BHO deaktiviert ist, funktionieren die WDS weiterhin ordnungsgemäß. Es ist jedoch nicht möglich, den Desktop auf einer Webseite zu durchsuchen.

Bei beiden der folgenden Optionen zum Zulassen einer Desktop Suche wird die Suche lokal mit der registrierten Suchanwendung ausgeführt.

## <a name="registering-web-page-urls"></a>Registrieren von Webseiten-URLs

Die Registrierung enthält eine Liste der "zulässigen" Domänen-URLs, von denen WDS aufgerufen werden kann. Wenn Sie Ihre Webseiten einschließen möchten, müssen Sie Ihre Domänen-URL (s) als reg \_ SZ in der Registrierung wie folgt auflisten:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows-Desktop Suche** \\ **DSW** \\ **zulässig**\\*<number>* = <domainURL>

Dabei **<number>** ist sequenziell nummeriert, und **<domainURL>** ist die URL der Webseite, von der Sie WDS suchen möchten. Diese URL-Zeichenfolge kann das Platzhalter Sternchen \* am Anfang oder Ende der URL enthalten. Wenn die Zeichenfolge z \* . b. ". mydomain.com" lautet, können Sie eine WDS-Suche sowohl von https://www.mydomain.com als auch von Starten https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Aktivieren der Desktop Suche per URL

Eine weitere Option, die keinen Zugriff auf die Registrierung erfordert, ist die Verwendung der folgenden URL auf Ihren Webseiten:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

Where **Query** ist die URL-codierte Zeichenfolge, nach der der Benutzer sucht, einschließlich der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md) Begriffe.

 

 




