---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Entfernen von Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217981"
---
# <a name="removal-of-windows-mail"></a>Entfernen von Windows Mail

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -hoch  
**Häufigkeit** -hoch  









## <a name="description"></a>BESCHREIBUNG

Microsoft hat das Windows Mail-Hilfsprogramm als veraltet markiert und die API costartoutlookexpress deaktiviert. Die anderen e-Mail-APIs wurden als veraltet markiert und können in einer späteren Windows-Version entfernt werden. Die öffentlich dokumentierten APIs, die nicht als veraltet oder veraltet gekennzeichnet sind, werden jedoch weiterhin in Windows 7 funktionieren. Binärdateien bleiben in den Benutzer Systemen erhalten und können weiterhin über die APIs aufgerufen werden, insbesondere in den oben erwähnten Fällen. Außerdem verbleiben die e-Mail-Dateien (. eml) und Nachrichten Dateien (. NWS) des Benutzers auf dem System.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Das Entfernen von Windows Mail führt zu folgendem:

-   Alle Einstiegspunkte für Windows-e-Mail und-Kontakte (z. b. Startmenü, von Benutzern erstellte Verknüpfungen, Start > ausführen usw.) werden entfernt oder deaktiviert. Einige davon werden vollständig entfernt, andere schlagen bei dem Versuch, zu starten, fehl.
-   Alle DLLs werden in der Box ausgeliefert.
-   Öffentlich dokumentierte APIs funktionieren weiterhin wie in Windows Vista.
-   Alle APIs, die versuchen, die Hauptbenutzer Oberfläche des Browsers zu starten, wurden geändert, um einen automatischen Fehler zu erzeugen. Die Funktion gibt Erfolg zurück, zeigt jedoch nicht die Benutzeroberfläche für den Benutzer an. APIs, die andere Dialogfelder (z. b. Spooler oder das Dialogfeld "Konten") aufzurufen, zeigen die Benutzeroberfläche weiterhin an.
-   Protokollhandler (mailto, LDAP, News, sNews, NNTP) werden nicht mit Windows Mail oder Kontakten verknüpft. Wenn Sie versuchen, diese zu starten, wird ein Fehler Dialogfeld angezeigt, das Sie auf den Speicherort zeigt, an dem diese Zuordnungen auf ein anderes Programm festlegen können
-   Dateizuordnungen (. eml,. nws,. Contact,. Group,. wab,. P7C,. VFC) sind beschädigt oder deaktiviert. Wenn Sie versuchen, eine Datei mit diesen Erweiterungen zu öffnen, erhalten Kunden ein Dialogfeld mit anderen installierten apps, die Sie verwenden und auf eine Webseite verweisen können, die Lösungen anbietet.
-   Alle Benutzer Dateien (z. b. Kontakt Dateien oder Meldungen) verbleiben im Upgradeszenario im System.
-   Der Ordner "Contacts" ist standardmäßig ausgeblendet, sodass er von Kunden nicht angezeigt wird.
-   APIs werden in MSDN als veraltet markiert.
-   Die Datei Vorschau Funktion wurde entfernt.
-   Shellhooks im Kontextmenü werden entfernt
-   Die Datei Suchfunktion wurde entfernt.

## <a name="mitigation"></a>Minderung

Benutzer sollten Windows Live Mail oder ein anderes Mail Produkt installieren, das. eml-und nws-Dateien lesen kann.

## <a name="solution"></a>Lösung

Erkennen, ob ein Standard-e-Mail-Handler installiert ist. Wenn dies nicht der Wert ist, sollten Sie den Benutzer dazu informieren, Windows Live Mail oder ein anderes Produkt zu installieren, das. eml-und nws-Dateien lesen kann.

Entwerfen Sie keinen Code, der die Benutzeroberflächen-API von Windows Mail aufruft, da dies nicht funktioniert. Sie müssen weitere Möglichkeiten finden, um auf die EML-und nws-Dateien zuzugreifen. Außerdem müssen Sie, sobald dies möglich ist, ihre Abhängigkeit von allen anderen Windows Mail-APIs beenden.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

-   Testen Sie Ihre Anwendung in einer Windows 7-Umgebung, um sicherzustellen, dass die Anwendung nicht versucht, die UI-API aufzurufen.
-   Alternativ können Sie das Anwendungskompatibilitäts-Toolkit (Act) mithilfe von Windows Compatibility Evaluator (WCE) ausführen, um mögliche Probleme aufgrund der Veraltung dieser Funktionalität zu ermitteln.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Anwendungskompatibilitäts-Toolkit Download](/windows-hardware/get-started/adk-install)  
</dl>

 

 
