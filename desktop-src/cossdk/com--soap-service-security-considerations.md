---
description: Sicherheitsüberlegungen zum COM+-SOAP-Dienst
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Sicherheitsüberlegungen zum COM+-SOAP-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67e034dfeaa4ec7f8688420aafcaec434653c942665ec3e3cbaa1535b51980d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548549"
---
# <a name="com-soap-service-security-considerations"></a>Sicherheitsüberlegungen zum COM+-SOAP-Dienst

Der COM+-SOAP-Dienst ist aus Sicherheitsgründen vom IIS-Webserver abhängig. Selbst im [vom Client aktivierten Objektmodus](accessing-xml-web-services-in-cao-mode.md)überträgt ein COM+-RPC die Clientidentität nicht und kann daher keine rollenbasierte Sicherheit oder ein anderes von DCOM bereitgestelltes Sicherheitsfeature verwenden. Wenn Sie zum Schutz des Datenschutzes von Daten beitragen möchten, die an und von Ihrem XML-Webdienst übertragen werden, oder um Ihren XML-Webdienst vor nicht autorisiertem Zugriff zu schützen, können Sie IIS so konfigurieren, dass der Zugriff auf einen XML-Webdienst basierend auf einer Client-IP-Adresse beschränkt wird oder ein Client ein digitales Zertifikat zur Überprüfung seiner Identität vorlegt. Wenn Sie den Zugriff nicht einschränken, kann jeder Client, der mit Ihrem Webserver kommunizieren kann, auf Ihren XML-Webdienst zugreifen.

Sie können IIS so konfigurieren, dass ihre XML-Webdienstkommunikation mit Clients mithilfe von SSL- oder TLS-Protokollen mit öffentlichem Schlüssel verschlüsselt wird. Wenn Sie die SOAP-Kommunikation nicht verschlüsseln, können zwischen einem Client und einem Server ausgetauschte Daten von einem Drittanbieter beobachtet werden, der Zugriff auf ein beliebiges Netzwerk hat, über das die SOAP-Kommunikation übertragen wird. Je nach Netzwerktopologie kann dies ein kleines LAN oder das Internet sein.

Standardmäßig werden unverschlüsselte SOAP-Kommunikationen am HTTP-Port (80) und verschlüsselte SOAP-Kommunikationen am HTTPS-Port (443) empfangen. Damit ein Client erfolgreich auf einen XML-Webdienst zugreifen kann, müssen alle Firewalls zwischen dem Client und dem Server so konfiguriert werden, dass TCP SYN-Pakete den entsprechenden Serverport erreichen können. Umgekehrt kann ein Firewalladministrator diese Ports schließen, um den Zugriff auf XML-Webdienste einzuschränken.

Die Standardsicherheitseinstellungen für eine COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, unterscheiden sich je nachdem, welche Version des Microsoft .NET Framework installiert ist. Wenn Version 1.0 installiert ist, sind XML-Webdienste standardmäßig unsicher. alle Aufrufe werden akzeptiert, und es wird keine Verschlüsselung verwendet. Wenn Version 1.1 oder höher installiert ist, sind XML-Webdienste standardmäßig sicher. Aufrufer müssen authentifiziert werden, und verschlüsselung ist erforderlich.

Ein geschützter XML-Webdienst unterstützt keinen WKO-Zugriff über WSDL. Clients, die die .NET Framework Version 1.1 installiert haben, können sie stattdessen im CAO-Modus aufrufen. Wenn Drittanbieterclients über WSDL auf Ihren XML-Webdienst zugreifen müssen, müssen Sie den anonymen Zugriff zulassen.

Eine COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, wird standardmäßig mit den Berechtigungen des anonymen Benutzers ausgeführt (nicht mit den Berechtigungen des Aufrufers). Sie können IIS so konfigurieren, dass der XML-Webdienst als anderer Benutzer ausgeführt wird. Dies kann manchmal erforderlich sein, da Ihre Komponente Dateien oder andere Ressourcen verwendet, auf die der anonyme Benutzer keinen Zugriff hat. Dennoch sollten Sie immer versuchen, Ihre Komponente mit möglichst wenigen Berechtigungen auszuführen, um den Schaden zu begrenzen, den ein böswilliger Aufrufer verursachen könnte.

> [!Note]  
> Da eine Methode, die Sie über einen XML-Webdienst verfügbar gemacht haben, potenziell für böswillige Aufrufer verfügbar gemacht werden kann, sollten Sie immer sicherstellen, dass Sie alle Eingabeparameter überprüfen, von denen sie abhängt.

 

Ausführliche Anweisungen zum Konfigurieren bestimmter SICHERHEITSeinstellungen für XML-Webdienste finden Sie unter [Sichern von XML-Webdiensten.](securing-xml-web-services.md)

**So konvertieren Sie eine sichere SOAP-Anwendung in eine unsichere SOAP-Anwendung**

1.  Öffnen Sie das Internetinformationsdienste-Verwaltungstool (IIS).
2.  Suchen Sie das virtuelle Verzeichnis für die Anwendung, und öffnen Sie das Dialogfeld **Eigenschaften.**
3.  Aktivieren Sie auf der Registerkarte **Dokumente** die **Option Standardinhalt aktivieren.**
4.  Klicken Sie auf der Registerkarte **Verzeichnissicherheit** unter **Anonymer Zugriff und Authentifizierungssteuerung** auf **Bearbeiten.**
5.  Aktivieren Sie **Anonymer Zugriff,** um den anonymen Zugriff zu aktivieren, und klicken Sie auf **OK.**
6.  Klicken Sie unter **Sichere Kommunikation** auf **Bearbeiten.**
7.  Deaktivieren Sie das Kontrollkästchen **Sicheren Kanal anfordern (SSL).**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> </dl>

 

 



