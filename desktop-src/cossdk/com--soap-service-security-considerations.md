---
description: Sicherheitsüberlegungen für COM+-SOAP-Dienste
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Sicherheitsüberlegungen für COM+-SOAP-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861635"
---
# <a name="com-soap-service-security-considerations"></a>Sicherheitsüberlegungen für COM+-SOAP-Dienste

Der com+-SOAP-Dienst hängt von der Sicherheit des IIS-Webservers ab. Selbst im vom [Client aktivierten Objekt Modus](accessing-xml-web-services-in-cao-mode.md)überträgt ein com+-RPC die Client Identität nicht und kann daher keine rollenbasierte Sicherheit oder andere von DCOM bereitgestellte Sicherheitsfunktionen nutzen. Wenn Sie den Schutz der Daten schützen möchten, die an und von Ihrem XML-Webdienst übermittelt werden, oder um Ihren XML-Webdienst vor unbefugtem Zugriff zu schützen, können Sie IIS so konfigurieren, dass der Zugriff auf einen XML-Webdienst auf der Grundlage der IP-Adresse einer Clients beschränkt wird oder dass ein Client ein digitales Zertifikat zur Überprüfung der Identität zur Verfügung stellt. Wenn Sie den Zugriff nicht einschränken, kann jeder Client, der mit dem Webserver kommunizieren kann, auf den XML-Webdienst zugreifen.

Sie können IIS so konfigurieren, dass die Kommunikation zwischen dem XML-Webdienst und-Clients mithilfe von SSL-oder TLS-Protokollen für öffentliche Schlüssel verschlüsselt wird. Wenn Sie die SOAP-Kommunikation nicht verschlüsseln, können die zwischen einem Client und einem Server ausgetauschten Daten von einem Drittanbieter mit Zugriff auf ein beliebiges Netzwerk, über das die SOAP-Kommunikation übertragen wird, beobachtet werden. abhängig von der Netzwerktopologie kann es sich hierbei um ein kleines LAN oder um das Internet handeln.

Standardmäßig werden unverschlüsselte SOAP-Kommunikationen am HTTP-Port (80) empfangen, und verschlüsselte SOAP-Kommunikationen werden am HTTPS-Port (443) empfangen. Damit ein Client erfolgreich auf einen XML-Webdienst zugreifen kann, müssen alle Firewalls zwischen dem Client und dem Server so konfiguriert werden, dass TCP-SYN-Pakete den entsprechenden Serverport erreichen können. Umgekehrt kann ein Firewalladministrator diese Ports schließen, um den Zugriff auf XML-Webdienste einzuschränken.

Die Standard Sicherheitseinstellungen für eine COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, unterscheiden sich abhängig davon, welche Version von Microsoft .NET Framework installiert ist. Wenn Version 1,0 installiert ist, sind XML-Webdienste standardmäßig nicht sicher. alle Aufrufe werden akzeptiert, und es wird keine Verschlüsselung verwendet. Wenn Version 1,1 oder höher installiert ist, sind XML-Webdienste standardmäßig sicher. Aufrufer müssen authentifiziert werden, und Verschlüsselung ist erforderlich.

Ein geschützter XML-Webdienst unterstützt den WKO-Zugriff über WSDL nicht. Stattdessen können Clients, auf denen die .NET Framework Version 1,1 installiert ist, im Modus "Cao" aufgerufen werden. Wenn Clients von Drittanbietern über WSDL auf Ihren XML-Webdienst zugreifen müssen, müssen Sie den anonymen Zugriff zulassen.

Eine COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, wird standardmäßig mit den Berechtigungen des anonymen Benutzers (nicht mit den Berechtigungen des Aufrufers) ausgeführt. Sie können IIS so konfigurieren, dass der XML-Webdienst als anderer Benutzer ausgeführt wird. Dies kann manchmal notwendig sein, da die Komponente Dateien oder andere Ressourcen verwendet, auf die der anonyme Benutzer keinen Zugriff hat. Dennoch sollten Sie immer versuchen, die Komponente mit möglichst wenigen Berechtigungen auszuführen, um den Schaden einzuschränken, den ein böswilliger Aufrufer verursachen könnte.

> [!Note]  
> Da eine Methode, die Sie über einen XML-Webdienst verfügbar gemacht haben, potenziell für böswillige Aufrufer verfügbar gemacht werden kann, sollten Sie immer sicherstellen, dass alle Eingabeparameter, von denen Sie abhängt,

 

Ausführliche Anweisungen zum Konfigurieren spezifischer Sicherheitseinstellungen für den XML-Webdienst finden Sie unter [Sichern von XML-Webdiensten](securing-xml-web-services.md).

**So konvertieren Sie eine sichere SOAP-Anwendung in eine unsichere SOAP-Anwendung**

1.  Öffnen Sie das Verwaltungs Tool für Internetinformationsdienste (IIS).
2.  Suchen Sie das virtuelle Verzeichnis für die Anwendung, und öffnen Sie das Dialogfeld **Eigenschaften** .
3.  Aktivieren Sie auf der Registerkarte **Dokumente** die Option **Standard Inhalt aktivieren** .
4.  Klicken Sie auf der Registerkarte **Verzeichnis Sicherheit** unter **Anonyme Zugriffs-und Authentifizierungs Steuerung** auf **Bearbeiten** .
5.  Überprüfen Sie den **anonymen** Zugriff auf den anonymen Zugriff, und klicken Sie auf **OK**
6.  Klicken Sie unter **sichere Kommunikation** auf **Bearbeiten** .
7.  Deaktivieren Sie das Kontrollkästchen **Secure Channel (SSL) erforderlich** .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> </dl>

 

 



