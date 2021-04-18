---
description: Wenn die Anwendung keine dll, Erweiterung, kein Plug-in oder Systemsteuerung hostet, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352341"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen

Wenn die Anwendung keine dll, Erweiterung, kein Plug-in oder Systemsteuerung hostet, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren. Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen mit Erweiterungen finden Sie unter [Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**So aktivieren Sie eine Assembly in einer Anwendung ohne gehostete Komponenten**

1.  Erstellen Sie ein Manifest, das die Abhängigkeit von der Anwendung oder Erweiterung in der Assembly beschreibt.

    Beispielsweise kann das Manifest für "yourapplication" erstellt werden, indem das folgende Beispiel Manifest kopiert und die richtigen Werte für **assemblyIdentity**, **ProcessorArchitecture** und **Description** ersetzt werden. Legen Sie den Wert von **ProcessorArchitecture** auf x86 fest, wenn Sie auf einer 32-Bit-Plattform aufbauen, und auf ia64, wenn Sie auf einer 64-Bit-Plattform aufbauen. Das **Description** -Element enthält eine options Beschreibung der Anwendung. Weitere Informationen zum Manifest-Format finden Sie unter [Anwendungs Manifeste](application-manifests.md).

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

2.  Fügen Sie das Manifest der Anwendung als Ressource in der binären ausführbaren Header Datei der Anwendung hinzu. Es wird nicht empfohlen, das Manifest als externe Manifest-Datei der Anwendung hinzuzufügen.

    Um das Manifest als Ressource hinzuzufügen, erstellen Sie eine Ressource in der Anwendung des Typs RT \_ Manifest ID 1. Wenn der Name der Anwendung beispielsweise yourapp lautet, sollte die Header Datei der Anwendung Folgendes enthalten:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Wenn Sie das Manifest stattdessen als externe Manifest-Datei hinzufügen, stellen Sie sicher, dass die-Installation die Manifest-Datei in den Ordner kopiert, der die ausführbare Datei der Anwendung enthält.

3.  Testen Sie, um sicherzustellen, dass von der Anwendung verwendete Assemblys in der Anwendung ordnungsgemäß funktionieren.

 

 



