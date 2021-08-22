---
description: Wenn Ihre Anwendung keine DLL, Erweiterung, Plug-In oder Systemsteuerung hosten soll, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142253"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen

Wenn Ihre Anwendung keine DLL, Erweiterung, Plug-In oder Systemsteuerung hosten soll, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren. Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen mit Erweiterungen finden Sie unter [Enabling an Assembly in an Application Hosting a DLL, Extension, or Systemsteuerung](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**So aktivieren Sie eine Assembly in einer Anwendung ohne gehostete Komponenten**

1.  Erstellen Sie ein Manifest, das die Abhängigkeit der Anwendung oder Erweiterung von der Assembly beschreibt.

    Beispielsweise kann das Manifest für "YourApplication" erstellt werden, indem das folgende Beispielmanifest kopiert und die richtigen Werte für **assemblyIdentity,** **processorArchitecture** und description durch die Werte von substituiert **werden.** Legen Sie den Wert von **processorArchitecture** auf x86 fest, wenn Sie auf einer 32-Bit-Plattform erstellen, und auf ia64, wenn Sie auf einer 64-Bit-Plattform erstellen. Das **description-Element** enthält eine Optionsbeschreibung der Anwendung. Weitere Informationen zum Manifestformat finden Sie unter [Anwendungsmanifesten.](application-manifests.md)

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Fügen Sie das Manifest der Anwendung als Ressource in der binären ausführbaren Headerdatei der Anwendung hinzu. Es wird nicht empfohlen, das Manifest der Anwendung als externe Manifestdatei hinzuzufügen.

    Um das Manifest als Ressource hinzuzufügen, erstellen Sie eine Ressource in der Anwendung vom Typ RT \_ MANIFEST ID 1. Wenn der Name der Anwendung beispielsweise YourApp ist, sollte die Headerdatei der Anwendung Folgendes enthalten:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Wenn Sie stattdessen das Manifest als externe Manifestdatei hinzufügen, stellen Sie sicher, dass die Installation die Manifestdatei in den Ordner kopiert, der die ausführbare Datei der Anwendung enthält.

3.  Testen Sie , um sicherzustellen, dass assemblys, die von der Anwendung verwendet werden, ordnungsgemäß in der Anwendung funktionieren.

 

 



