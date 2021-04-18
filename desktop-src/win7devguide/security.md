---
title: Sicherheit (Windows 7-Entwicklerhandbuch)
description: Windows 7 bietet neue und verbesserte Sicherheitsfeatures, die es Entwicklern erleichtern, die Sicherheit Ihrer Anwendungen zu verbessern, zu verwenden und zu verwalten.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339108"
---
# <a name="security-windows-7-developer-guide"></a>Sicherheit (Windows 7-Entwicklerhandbuch)

Windows 7 bietet neue und verbesserte Sicherheitsfeatures, die es Entwicklern erleichtern, die Sicherheit Ihrer Anwendungen zu verbessern, zu verwenden und zu verwalten. Es verfügt über eine Reihe neuer Sicherheitsfeatures, die nicht nur den Schutz vor Bedrohungen erleichtern, sondern auch den Schaden begrenzen, den Angreifer durchführen können, wenn Sie Zugriff auf einen Computer erhalten.

Dank der Verbesserungen an der Windows-Filter Plattform können Entwickler Anwendungen erstellen, die mit der Paketverarbeitung im Netzwerk Stapel des Betriebssystems interagieren. Netzwerkdaten können gefiltert und auch geändert werden, bevor sie ihr Ziel erreichen.

Außerdem kann die Systemsicherheit aufgrund von Änderungen am Windows-Berechtigungs Modell von Entwicklern und Ihren Endbenutzern leichter verwaltet werden. Neue Verbesserungen erleichtern die Identifizierung kritischer Eingabe Aufforderungen, um sicherzustellen, dass Benutzer auf die Anwendungen und Features zugreifen können, die Sie benötigen, ohne deren Systeme zu beeinträchtigen (Weitere Informationen finden Sie im [MSDN Security Developer Center](https://msdn.microsoft.com/security/default.aspx).)

## <a name="windows-filtering-platform"></a>Windows-Filterplattform

In Windows 7 wurde die Windows-Filter Plattform verbessert, um Entwicklern eine bessere Kontrolle über die Firewallfunktionalität zu verschaffen. Die Filter Ebene wurde erweitert, und *ISVs* können jetzt benutzerdefinierten Schutz und Erkennung auf niedrigeren Ebenen einbinden. Außerdem können firewallentwickler Teile der Windows-Firewall selektiv aktivieren oder deaktivieren.

Mithilfe der Windows-Filter Plattform können Entwickler Firewalls, Angriffs Erkennungssysteme, Antivirenprogramme, Netzwerk Überwachungstools und Jugend Steuerungsmechanismen in Ihren Anwendungen erstellen. Die Windows-Filter Plattform ist in integriert und bietet Unterstützung für eine Vielzahl von Firewallfeatures, einschließlich authentifizierter Kommunikation und dynamischer Firewallkonfiguration basierend auf der Verwendung der Sockets-API (Anwendungs basierte Richtlinie) der Anwendungen. Die Windows-Filter Plattform bietet auch eine Infrastruktur für die Richtlinien Verwaltung, Änderungs Benachrichtigungen, Netzwerk Diagnose und Zustands behaftete Filterung.

Die ursprüngliche Architektur der Windows-Filter Plattform in Windows Vista bot Funktionen für IP-basierten Datenverkehr. Andere nicht-IP-Protokolle, wie z. b. die Protokolle Address Resolution Protocol (ARP) und Media Access Control (*Mac*)-Schicht für Netzwerkverwaltung und Authentifizierung, erfordern auch Filterung, Überprüfung oder Protokollierung. In Windows 7 wurde eine *NDIS* -Inspektions Schicht, die *Mac* -und *Ethernet* -Filterung unterstützt, bereitgestellt, um diese Anforderung zu erfüllen. (Weitere Informationen finden Sie unter [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Die Benutzerkontensteuerung (User Account Control, UAC) ist eine Sicherheitskomponente in Windows 7, mit der Entwickler Anwendungen erstellen können, die es Benutzern ermöglichen, gängige Aufgaben als nicht-Administratoren auszuführen. Entwickler können Sicherheitsrisiken verringern, indem Sie Anwendungen unter einem Standardbenutzer Token ausführen und so das Risiko von Fehlern oder Angriffen verringern.

Benutzerkonten, die Mitglieder der lokalen *Administrator* Gruppe sind, führen die meisten Anwendungen als Standardbenutzer aus. Durch die Trennung von Benutzer-und Administrator Funktionen bei gleichzeitiger Aktivierung der Produktivität ermöglicht die Benutzerkontensteuerung Entwicklern eine bessere Kontrolle über die Zugriffsebene, die Benutzer über geschützte Anwendungsbereiche haben. UAC fordert Anmelde Informationen in einem *sicheren Desktop* Modus an, in dem der gesamte Bildschirm geschützt ist, um das Spoofing der Benutzeroberfläche oder der Maus zu verhindern. (Weitere Informationen finden Sie unter [Benutzerkontensteuerung](../win7appqual/user-interface---user-account-control-dialog-updates.md) und [Benutzerkontensteuerung und WMI](../wmisdk/user-account-control-and-wmi.md).)

 

 
