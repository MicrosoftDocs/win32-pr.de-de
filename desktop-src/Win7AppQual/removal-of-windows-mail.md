---
description: Entfernen von Windows-E-Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Entfernen von Windows-E-Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116278"
---
# <a name="removal-of-windows-mail"></a>Entfernen von Windows-E-Mail

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Hoch  
**Häufigkeit** – Hoch  









## <a name="description"></a>BESCHREIBUNG

Microsoft stellt das Windows Mail-Hilfsprogramm als veraltet ein und deaktiviert die API CoStartOutlookExpress. Die anderen E-Mail-APIs wurden als veraltet markiert und werden in einer späteren Windows-Version entfernt. Die öffentlich dokumentierten APIs, die nicht als veraltet oder veraltet markiert sind, funktionieren in Windows 7 jedoch weiterhin. Binärdateien verbleiben auf den Systemen der Benutzer und sind weiterhin über die APIs zugänglich, insbesondere in den oben genannten Fällen. Darüber hinaus verbleiben die E-Mail- (EML) und News-Dateien (.nws) der Benutzer auf dem System.

## <a name="manifestation-of-impact"></a>Auswirkungen

Das Entfernen von Windows Mail führt zu Folgendem:

-   Alle Einstiegspunkte für Windows-E-Mail und -Kontakte (z. B. Startmenü, vom Benutzer erstellte Verknüpfungen, Start -> Ausführen und so weiter) werden entfernt oder deaktiviert. Einige davon werden vollständig entfernt, andere werden beim Versuch, gestartet zu werden, fehlschlagen.
-   Alle DLLs sind im Feld
-   Öffentlich dokumentierte APIs funktionieren weiterhin wie in Windows Vista
-   Alle APIs, die versuchen, die Hauptbenutzeroberfläche des Browsers zu starten, wurden geändert, um einen automatischen Fehler zu erstellen. Die Funktion gibt den Erfolg zurück, zeigt dem Benutzer jedoch nicht die Benutzeroberfläche an. APIs, die andere Dialogfelder aufrufen (z. B. der Spooler oder das Dialogfeld Konten), zeigen diese Benutzeroberfläche weiterhin an.
-   Protokollhandler (mailto, ldap, news, sara, nntp) werden windows-E-Mail oder -Kontakten nicht zugeordnet. Wenn Sie versuchen, diese zu starten, wird kunden ein Fehlerdialogfeld angezeigt, das sie auf den Speicherort der Zuordnungen zu einem anderen Programm verweisen kann.
-   Dateizuordnungen (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sind beschädigt oder deaktiviert. Wenn Sie versuchen, eine Datei mit diesen Erweiterungen zu öffnen, erhalten Kunden ein Dialogfeld, das ihnen andere installierte Apps anbietet, die sie verwenden und auf eine Webseite verweisen können, die Lösungen anbietet.
-   Alle Benutzerdateien (z. B. Kontaktdateien oder Nachrichten) verbleiben im Upgradeszenario auf dem System.
-   Der Ordner "Kontakte" ist standardmäßig ausgeblendet, sodass Kunden ihn nicht sehen.
-   APIs sind in MSDN als veraltet markiert.
-   Die Dateivorschaufunktion wurde entfernt.
-   Shellhooks im Kontextmenü werden entfernt.
-   Die Dateisuchfunktion wurde entfernt.

## <a name="mitigation"></a>Minderung

Benutzer sollten Windows Live Mail oder ein anderes E-Mail-Produkt installieren, das EML- und NWS-Dateien lesen kann.

## <a name="solution"></a>Lösung

Ermitteln Sie, ob ein Standard-E-Mail-Handler installiert ist. Wenn dies nicht der Fall ist, empfehlen Sie dem Benutzer, Windows Live Mail oder ein anderes Produkt zu installieren, das EML- und NWS-Dateien lesen kann.

Entwerfen Sie keinen Code, der die Windows Mail-UI-API aufruft, da sie nicht funktioniert. Sie müssen andere Möglichkeiten für den Zugriff auf die EML- und NWS-Dateien finden. Stellen Sie außerdem, sobald dies möglich ist, ihre Abhängigkeit von allen anderen Windows Mail-APIs ein.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests

-   Führen Sie Ihre Anwendung in einer Windows 7-Umgebung aus, um sicherzustellen, dass die Anwendung nicht versucht, die UI-API auf aufruft.
-   Alternativ können Sie das Application Compatibility Toolkit (ACT) mithilfe der Windows-Kompatibilitätsauswertung (Windows Compatibility Evaluator, WCE) ausführen, um mögliche Probleme zu ermitteln, die durch die Veralterung dieser Funktionalität bedingt sind.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Download des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)  
</dl>

 

 
