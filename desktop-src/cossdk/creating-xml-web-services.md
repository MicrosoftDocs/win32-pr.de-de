---
description: Jede com+-Anwendung kann als XML-Webdienst verfügbar gemacht werden.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Erstellen von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346228"
---
# <a name="creating-xml-web-services"></a>Erstellen von XML-Webdiensten

Jede com+-Anwendung kann als XML-Webdienst verfügbar gemacht werden. Die Methoden in den Standardschnittstellen der von Anwendungen konfigurierten Komponenten (Komponenten im com+-Katalog der Server) können dann Remote aufgerufen werden. Mit dem Verwaltungs Programmkomponenten Dienste können Sie ein virtuelles IIS-Stammverzeichnis erstellen, aus dem die Komponenten Methoden mithilfe von SOAP aufgerufen werden können.

> [!Note]  
> Die .NET Framework muss auf Ihrem Computer installiert sein, um eine COM+-Anwendung als XML-Webdienst verfügbar zu machen.

 

**So machen Sie eine COM+-Anwendung als XML-Webdienst verfügbar**

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **Eigenschaften** aus.

3.  Klicken Sie im Dialogfeld Eigenschaften auf die Registerkarte **Aktivierung** .

4.  Aktivieren Sie das Kontrollkästchen **verwendet SOAP** .

5.  Geben Sie im Textfeld **SOAP-vroot** den Namen des virtuellen IIS-Stamm Verzeichnisses ein, von dem aus auf die Komponenten Methoden Remote zugegriffen werden kann. Beachten Sie, dass ein SOAP-vroot kein Unterverzeichnis eines anderen SOAP-vroot-Verzeichnisses sein kann.

6.  Klicken Sie auf **OK**.

    Wenn Sie das virtuelle IIS-Stammverzeichnis als *vroot* angeben und der voll qualifizierte Domänen Name des Servers Server *Name* ist, lautet die URL, unter der die Komponente als XML-Webdienst verfügbar gemacht wird, https://*Server* Name / *vroot*/.

    Das entsprechende Verzeichnis im Dateisystem ist \\ Windows \\ system32 \\ com \\ soapvroots \\ *vroot* \\ ; Com+ platziert mehrere Konfigurationsdateien und ASP.net-Programme. Für einen XML-Webdienst, der stark ausgelastet ist, können Sie die in der Datei web.config gespeicherten Parameter anpassen. Weitere Informationen zu dieser Datei finden Sie in der IIS-Dokumentation.

    Die Standard Sicherheitseinstellungen für eine COM+-Anwendung, die als XML-Webdienst verfügbar gemacht wird, unterscheiden sich abhängig davon, welche Version des .NET Framework installiert ist. Wenn Version 1,0 installiert ist, sind XML-Webdienste standardmäßig nicht sicher. alle Aufrufe werden akzeptiert, und es wird keine Verschlüsselung verwendet. Wenn Version 1,1 oder höher installiert ist, sind XML-Webdienste standardmäßig sicher. Aufrufer müssen authentifiziert werden, und Verschlüsselung ist erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im Modus "Cao"](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 



