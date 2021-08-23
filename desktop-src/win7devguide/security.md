---
title: Sicherheit (Windows 7 Entwicklerhandbuch)
description: Windows 7 enthält neue und verbesserte Sicherheitsfeatures, die Es Entwicklern erleichtern, die Sicherheit ihrer Anwendungen zu verbessern, zu verwenden und zu verwalten.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421256c23042ad1ea4bad57a616047e43276449bd93f771543d4eb41286c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329740"
---
# <a name="security-windows-7-developer-guide"></a>Sicherheit (Windows 7 Entwicklerhandbuch)

Windows 7 enthält neue und verbesserte Sicherheitsfeatures, die Es Entwicklern erleichtern, die Sicherheit ihrer Anwendungen zu verbessern, zu verwenden und zu verwalten. Es verfügt über eine Vielzahl neuer Sicherheitsfeatures, die nicht nur zum Schutz vor Bedrohungen beitragen, sondern auch den Schaden begrenzen, den Angreifer beim Zugriff auf einen Computer verursachen können.

Verbesserungen an der Windows Filtering Platform ermöglichen Es Entwicklern, Anwendungen zu erstellen, die mit der Paketverarbeitung im Netzwerkstapel des Betriebssystems interagieren. Netzwerkdaten können gefiltert und auch geändert werden, bevor sie ihr Ziel erreichen.

Außerdem ist die Systemsicherheit aufgrund von Änderungen am Windows-Berechtigungsmodells sowohl für Entwickler als auch für deren Endbenutzer besser verwaltbar. Neue Verbesserungen machen es einfach, kritische Eingabeaufforderungen zu identifizieren, um sicherzustellen, dass Benutzer auf die benötigten Anwendungen und Features zugreifen können, ohne ihre Systeme zu gefährden. (Weitere Informationen finden Sie [im MSDN Security Developer Center.)](https://msdn.microsoft.com/security/default.aspx)

## <a name="windows-filtering-platform"></a>Windows-Filterplattform

In Windows 7 wurde die Windows-Filterplattform erweitert, um Entwicklern mehr Kontrolle über die Firewallfunktionalität zu geben. Die Filterebene wurde erhöht, und *ISVs* können jetzt benutzerdefinierten Schutz und die Erkennung auf niedrigeren Ebenen aktivieren. Darüber hinaus können Firewallentwickler Teile der Firewall Windows aktivieren oder deaktivieren.

Mit Windows Filterplattform können Entwickler Firewalls, Angriffserkennungssysteme, Antivirenprogramme, Netzwerküberwachungstools und Jugendkontrollen in ihre Anwendungen integrieren. Windows Die Filterplattform ist in integriert und bietet Unterstützung für eine Vielzahl von Firewallfeatures, einschließlich authentifizierter Kommunikation und dynamischer Firewallkonfiguration basierend auf der Verwendung der Sockets-API (anwendungsbasierte Richtlinie) durch Anwendungen. Windows Die Filterplattform bietet auch Infrastruktur für richtlinienverwaltung, Änderungsbenachrichtigungen, Netzwerkdiagnose und zustandshafte Filterung.

Die anfängliche Architektur der Windows-Filterplattform in Windows Vista bietet Funktionen für IP-basierten Datenverkehr. Andere Nicht-IP-Protokolle, z. B. ARP (Address Resolution Protocol) und Mac-Schichtprotokolle *(Media* Access Control, Medienzugriffssteuerung) für die Netzwerkverwaltung und -Authentifizierung, erfordern ebenfalls Filterung, Überprüfung oder Protokollierung. In Windows 7 wurde eine *NDIS-Überprüfungsebene* bereitgestellt, die *MAC-* und *ETHERNET-Filterung* unterstützt, um diese Anforderungen zu erfüllen. (Siehe [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Die Benutzerkontensteuerung (User Account Control, UAC) ist eine Sicherheitskomponente in Windows 7, mit der Entwickler Anwendungen erstellen können, mit denen Benutzer allgemeine Aufgaben als Nichtadministratoren ausführen können. Entwickler können Sicherheitsrisiken verringern, indem sie Anwendungen unter einem Standardbenutzertoken ausführen, um das Risiko von Fehlern oder Angriffen zu verringern.

Benutzerkonten, die Mitglieder der lokalen *Administratorgruppe* sind, führen die meisten Anwendungen als Standardbenutzer aus. Durch die Trennung von Benutzer- und Administratorfunktionen bei gleichzeitiger Produktivitätssteigerung erhalten Entwickler mit UAC mehr Kontrolle über die Zugriffsebene, die Benutzer über geschützte Bereiche einer Anwendung haben. UAC fordert Anmeldeinformationen in einem *Sicheren Desktopmodus* an, in dem der gesamte Bildschirm geschützt ist, um spoofing der Benutzeroberfläche oder der Maus zu verhindern. (Weitere Informationen [finden Sie unter Dialogfeldupdates zur Benutzerkontensteuerung](../win7appqual/user-interface---user-account-control-dialog-updates.md) [und Benutzerkontensteuerung und WMI.)](../wmisdk/user-account-control-and-wmi.md)

 

 
