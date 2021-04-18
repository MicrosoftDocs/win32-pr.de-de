---
description: Wenn Ihre Anwendung eine Drittanbieter-DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung hostet, können Sie eine Assembly in der Anwendung&8212 aktivieren, \# ohne diese Assembly auch für die gehosteten Komponenten aktivieren zu müssen.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357813"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet

Wenn Ihre Anwendung eine Drittanbieter-DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung hostet, empfiehlt es sich, eine Assembly in Ihrer Anwendung zu aktivieren – ohne diese Assembly für die gehosteten Komponenten aktivieren zu müssen. Dies kann der Fall sein, wenn eine gehostete Komponente Codeänderungen erfordert, um die Assembly zu verwenden. Als Anwendungsentwickler können Sie möglicherweise keine Änderungen an diesen Komponenten von Drittanbietern vornehmen. In diesem Fall sollten Sie das in diesem Abschnitt beschriebene Verfahren befolgen, damit Ihre Anwendung die Assembly verwenden kann, ohne dass sich dies auf die gehosteten Komponenten auswirkt.

-   Um eine Assembly in einer Anwendung ohne Auswirkungen auf gehostete DLLs, Erweiterungen, Plug-ins oder Steuerelemente zu aktivieren, sollte ein Manifest, das die Abhängigkeit der Anwendung von der Assembly beschreibt, in der Anwendung als Ressource enthalten sein. Die gehosteten Komponenten, die nicht mit der Assembly aktiviert werden, sollten keine Manifeste einschließen, in denen diese Abhängigkeit beschrieben wird.
-   Um eine Assembly in einer Anwendung und ihren gehosteten DLLs, Erweiterungen, Plug-ins oder Steuerelementen zu aktivieren, schließen Sie Manifeste als Ressourcen in die Anwendung und die zugehörigen gehosteten Komponenten ein. Die in der Anwendung und in den gehosteten Komponenten enthaltenen Manifeste sollten jeweils eine Abhängigkeit von der Assembly beschreiben. In der Regel fügt der Anwendungsentwickler der Anwendung ein Manifest hinzu, und der Entwickler der gehosteten Komponente fügt der dll, Erweiterung, dem Plug-in oder der Systemsteuerung ein Manifest hinzu.

Die folgende Methode kann verwendet werden, um einer Anwendung oder einer gehosteten Komponente, bei der es sich um eine DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung handelt, ein Manifest hinzuzufügen.

**Zum Aktivieren einer Assembly in einer Anwendung oder einer gehosteten Komponente.**

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

2.  Erstellen Sie eine Ressource in der Anwendung oder Erweiterung des Typs RT \_ Manifest ID 2.

    Wenn der Name der Anwendung beispielsweise yourapp lautet, sollte die Anwendung Folgendes enthalten:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Kompilieren Sie die Anwendung mit dem Flag "-disolations \_ \_ fähig", oder fügen Sie diese Anweisung vor der \# include-Anweisung "Windows. h" ein. Im Fall einer Anwendung mit mehreren Modulen ist das Flag-disolations- \_ \_ fähig aktiviert für alle Module erforderlich.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Testen Sie, um sicherzustellen, dass die von der Anwendung verwendeten Assemblys in der Anwendung und der gehosteten Komponente ordnungsgemäß funktionieren.

Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen ohne Erweiterungen finden Sie unter [Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen](enabling-an-assembly-in-an-application-without-extensions.md).

 

 



