---
description: Entfernen von Windows E-Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Entfernen von Windows E-Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2456fa5bdf9d981385f2b4832250358f7bfdab1b223aeb3658d8df4cc212237b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328934"
---
# <a name="removal-of-windows-mail"></a>Entfernen von Windows E-Mail

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Hoch  
**Frequency** – High  









## <a name="description"></a>Beschreibung

Microsoft setzt das hilfsprogramm Windows Mail als veraltet ein und deaktiviert die API CoStartOutlookExpress. Die anderen E-Mail-APIs wurden als veraltet markiert und werden in einer späteren Windows Version entfernt. Die öffentlich dokumentierten APIs, die nicht als veraltet oder veraltet gekennzeichnet sind, funktionieren jedoch weiterhin in Windows 7. Binärdateien verbleiben auf den Systemen der Benutzer und sind weiterhin über die APIs zugänglich, insbesondere in den oben genannten Fällen. Darüber hinaus verbleiben die E-Mail-Dateien (EML) und Nachrichtendateien (.nws) der Benutzer im System.

## <a name="manifestation-of-impact"></a>Auswirkungen

Das Entfernen von Windows Mail führt zu folgendem Ergebnis:

-   Alle Einstiegspunkte für Windows E-Mail und Kontakte (z. B. Startmenü, vom Benutzer erstellte Verknüpfungen, Start -> Ausführen usw.) werden entfernt oder deaktiviert. Einige davon werden vollständig entfernt, andere schlagen fehl, wenn sie versuchen, den Start zu starten.
-   Alle DLLs werden im Feld versendet.
-   Öffentlich dokumentierte APIs funktionieren weiterhin wie in Windows Vista
-   Alle APIs, die versuchen, die Hauptbrowserbenutzeroberfläche zu starten, wurden geändert, um einen automatischen Fehler zu erstellen. Die Funktion gibt erfolglos zurück, zeigt dem Benutzer jedoch nicht die Benutzeroberfläche an. APIs, die andere Dialogfelder aufrufen (z.B. der Spooler oder das Dialogfeld Konten), zeigen diese Benutzeroberfläche weiterhin an.
-   Protokollhandler (mailto, ldap, news, s ldap, nntp) werden nicht Windows Mail oder Contacts zugeordnet. Beim Versuch, diese zu starten, wird kunden ein Fehlerdialogfeld angezeigt, in dem sie auf den Speicherort verweisen, an dem sie diese Zuordnungen auf ein anderes Programm festlegen können.
-   Dateizuordnungen (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sind fehlerhaft oder deaktiviert. Wenn Sie versuchen, eine Datei mit diesen Erweiterungen zu öffnen, erhalten Kunden ein Dialogfeld, in dem sie anderen installierten Apps, die sie verwenden können, und sie auf eine Webseite verweisen, die Lösungen anbietet.
-   Alle Benutzerdateien (z. B. Kontaktdateien oder Nachrichten) verbleiben im Upgradeszenario auf dem System.
-   Der Ordner "Kontakte" ist standardmäßig ausgeblendet, sodass kunden ihn nicht sehen.
-   APIs sind in MSDN als veraltet markiert.
-   Die Dateivorschaufunktion wurde entfernt.
-   Shellhooks im Rechtsklickmenü werden entfernt.
-   Die Dateisuchfunktion wurde entfernt.

## <a name="mitigation"></a>Minderung

Benutzer sollten Windows Live Mail oder ein anderes E-Mail-Produkt installieren, das EML- und NWS-Dateien lesen kann.

## <a name="solution"></a>Lösung

Erkennen Sie, ob ein Standard-E-Mail-Handler installiert ist. Wenn dies nicht der Fall ist, raten Sie dem Benutzer, Windows Live Mail oder ein anderes Produkt zu installieren, das EML- und NWS-Dateien lesen kann.

Entwerfen Sie keinen Code, der die Windows-API für die E-Mail-Benutzeroberfläche aufruft, da er nicht funktioniert. Sie müssen andere Möglichkeiten finden, auf die EML- und NWS-Dateien zuzugreifen. Außerdem sollten Sie ihre Abhängigkeit von allen anderen Windows Mail-APIs einstellen, sobald dies möglich ist.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

-   Führen Sie Ihre Anwendung in einer Windows 7-Umgebung aus, um sicherzustellen, dass die Anwendung nicht versucht, die UI-API aufzurufen.
-   Alternativ können Sie das Application Compatibility Toolkit (ACT) mithilfe der Windows Compatibility Evaluator (WCE) ausführen, um mögliche Probleme aufgrund der Veraltung dieser Funktionalität zu ermitteln.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Herunterladen des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)  
</dl>

 

 
