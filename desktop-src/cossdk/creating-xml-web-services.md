---
description: Jede COM+-Anwendung kann als XML-Webdienst verfügbar gemacht werden.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Erstellen von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12dbc5ee08d9300d52b538648ba520b16a60a9e3769242c252eaa40d518a3ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307337"
---
# <a name="creating-xml-web-services"></a>Erstellen von XML-Webdiensten

Jede COM+-Anwendung kann als XML-Webdienst verfügbar gemacht werden. Die Methoden in den Standardschnittstellen der anwendungskonfigurierten Komponenten (Komponenten im COM+-Katalog der Server) können dann remote aufgerufen werden. Sie können das Verwaltungstool komponentendienste verwenden, um ein virtuelles IIS-Stammverzeichnis zu erstellen, aus dem die Komponentenmethoden mit SOAP aufgerufen werden können.

> [!Note]  
> Die .NET Framework muss auf Ihrem Computer installiert sein, um eine COM+-Anwendung als XML-Webdienst verfügbar zu machen.

 

**So machen Sie eine COM+-Anwendung als XML-Webdienst verfügbar**

1.  Öffnen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste unter Komponentendienste den **Ordner COM+-Anwendungen,** der dem computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **Eigenschaften aus.**

3.  Klicken Sie **im Eigenschaftendialogfeld** auf die Registerkarte Aktivierung.

4.  Aktivieren Sie das **Kontrollkästchen Soap** verwendet .

5.  Geben Sie **im Textfeld SOAP VRoot** den Namen des virtuellen IIS-Stammverzeichnisses ein, von dem aus remote auf die Komponentenmethoden zugegriffen werden kann. Beachten Sie, dass ein SOAP-VRoot kein Unterverzeichnis eines anderen SOAP VRoot-Verzeichnisses sein kann.

6.  Klicken Sie auf **OK**.

    Wenn Sie das virtuelle IIS-Stammverzeichnis als *vroot* angeben und der vollqualifizierte Domänenname Ihres Servers *servername* ist, wird die URL, unter der Ihre Komponente als XML-Webdienst verfügbar gemacht wird, https://*servername* / *vroot*/ angegeben.

    Das entsprechende Verzeichnis in Ihrem Dateisystem ist \\ windows \\ system32 \\ com \\ SoapVRoots \\ *vroot;* \\ COM+ platziert mehrere Konfigurationsdateien und ASP.NET Programme dort. Für einen XML-Webdienst mit starker Auslastung sollten Sie die in der Datei gespeicherten Parameter anpassen, web.config. Informationen zu dieser Datei finden Sie in der IIS-Dokumentation.

    Die Standardsicherheitseinstellungen für eine COM+-Anwendung, die als XML-Webdienst verfügbar gemacht wird, unterscheiden sich je nachdem, welche Version der .NET Framework installiert ist. Wenn Version 1.0 installiert ist, sind XML-Webdienste standardmäßig unsicher. alle Aufrufe werden akzeptiert, und es wird keine Verschlüsselung verwendet. Wenn Version 1.1 oder höher installiert ist, sind XML-Webdienste standardmäßig sicher. -Aufrufer müssen authentifiziert werden, und eine Verschlüsselung ist erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im CAO-Modus](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[ÜBERSICHT ÜBER DEN COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 



