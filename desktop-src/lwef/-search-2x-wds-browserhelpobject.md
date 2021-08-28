---
title: Aufrufen von WDS über Webseiten
description: Sie können Microsoft Windows Desktop Search (WDS) von jeder Webseite aufrufen, die Sie mithilfe des Browserhilfsobjekts (Browser Helper Object, BHO) und Windows Internet Explorer erstellen oder verwalten.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2be6be30889e8f759ee3cf7529250a5513ce58
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883711"
---
# <a name="calling-wds-from-web-pages"></a>Aufrufen von WDS über Webseiten

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

Sie können Microsoft Windows Desktop Search (WDS) von jeder Webseite aufrufen, die Sie mithilfe des Browserhilfsobjekts (Browser Helper Object, BHO) und Windows Internet Explorer erstellen oder verwalten. Wie dies funktioniert, erfahren Sie auf der MSN-Webseite. Über dem Suchfeld https://www.msn.com auf befinden sich mehrere Suchtypen: Web, News, Images, Desktop, Encarta und Local. Wenn Sie auf Desktop klicken, werden die Suchparameter an Windows Desktopsuche übergeben, die den Katalog durchsucht und Ergebnisse auf der WDS-Benutzeroberfläche anzeigt. Damit Benutzer eine Desktopsuche über Ihre Webseiten starten können, muss der WDSBHO auf ihren Systemen installiert und aktiviert sein, Ihre Webseiten müssen bei WDS als zulässige URL registriert sein, und Sie müssen einen Link erstellen, um die vom Benutzer initiierte Abfrage an WDS zu übergeben.

## <a name="enabling-the-wds-browser-help-object"></a>Aktivieren des WDS-Browserhilfeobjekts

Der BHO wird in Internet Explorer standardmäßig installiert und aktiviert, wenn Sie WDS installieren. Sie können jedoch problemlos überprüfen, ob er nicht deaktiviert oder deinstalliert wurde. Öffnen Sie auf dem System eines Benutzers Internet Explorer , wählen Sie im Menü **Extras** die Option **Internetoptionen** aus, klicken Sie auf die Registerkarte **Programme,** und klicken Sie dann auf **Add-Ons verwalten.** Suchen Sie in der Liste der Add-Ons nach der dsWebAllowBHO-Klasse, und stellen Sie sicher, dass sie aktiviert ist. Wenn der BHO deaktiviert ist, funktioniert WDS weiterhin normal. Sie können den Desktop jedoch nicht über eine Webseite durchsuchen.

Beide der folgenden Optionen zum Zulassen einer Desktopsuche führen die Suche lokal mit der registrierten Suchanwendung aus.

## <a name="registering-web-page-urls"></a>Registrieren von Webseiten-URLs

Die Registrierung enthält eine Liste der "zulässigen" Domänen-URLs, von denen WDS aufgerufen werden kann. Um Ihre Webseiten einzufügen, müssen Sie Ihre Domänen-URLs wie folgt als REG \_ SZ in der Registrierung auflisten:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **Allowed** \\ *&lt; number &gt;*  =  &lt; domainURL&gt;

Dabei ist **&lt; number &gt;** sequenziell nummeriert, und **&lt; domainURL &gt;** ist die URL der Webseite, von der aus Sie WDS-Suchvorgänge zulassen möchten. Diese URL-Zeichenfolge kann das Platzhalterzeichen am \* Anfang oder Ende der URL enthalten. Wenn die Zeichenfolge beispielsweise \* ".mydomain.com" lautet, können Sie eine WDS-Suche sowohl über als auch über https://www.mydomain.com https://mydomain.com starten.

## <a name="enabling-desktop-search-by-url"></a>Aktivieren der Desktopsuche nach URL

Eine weitere Option, die keinen Zugriff auf die Registrierung erfordert, ist die Verwendung der folgenden URL auf Ihren Webseiten:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

dabei ist **QUERY** die URL-codierte Zeichenfolge, nach der der Benutzer sucht, einschließlich aller Begriffe [der erweiterten Abfragesyntax.](-search-2x-wds-aqsreference.md)

 

 




