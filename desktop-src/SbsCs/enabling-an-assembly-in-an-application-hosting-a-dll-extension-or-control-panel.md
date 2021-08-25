---
description: Wenn Ihre Anwendung eine DLL, Erweiterung, ein Plug-In oder eine Systemsteuerung eines Drittanbieters hostet, sollten Sie eine Assembly in Ihrer Anwendung&8212; aktivieren, ohne diese Assembly auch für die gehosteten Komponenten zu \# aktivieren.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ac528c10d7ca0de903c6b132e0349c16061d63f121c390483458b4ef422d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885540"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung

Wenn Ihre Anwendung eine DLL, Erweiterung, ein Plug-In oder eine Systemsteuerung eines Drittanbieters hostet, sollten Sie eine Assembly in Ihrer Anwendung aktivieren, ohne diese Assembly auch für die gehosteten Komponenten zu aktivieren. Dies kann der Fall sein, wenn eine gehostete Komponente Codeänderungen erfordert, um die Assembly zu verwenden. Als Anwendungsentwickler können Sie möglicherweise keine Änderungen an diesen Drittanbieterkomponenten vornehmen. In diesem Fall sollten Sie das in diesem Abschnitt beschriebene Verfahren befolgen, damit Ihre Anwendung die Assembly verwenden kann, ohne die gehosteten Komponenten zu beeinträchtigen.

-   Um eine Assembly in einer Anwendung zu aktivieren, ohne dass gehostete DLLs, Erweiterungen, Plug-Ins oder Kontrollpanels betroffen sind, sollte ein Manifest, das die Abhängigkeit der Anwendung von der Assembly beschreibt, in die Anwendung als Ressource aufgenommen werden. Die gehosteten Komponenten, die nicht mit der Assembly aktiviert werden, sollten keine Manifeste enthalten, die diese Abhängigkeit beschreiben.
-   Um eine Assembly in einer Anwendung und ihren gehosteten DLLs, Erweiterungen, Plug-Ins oder Steuerungspanels zu aktivieren, schließen Sie Manifeste als Ressourcen in die Anwendung und ihre gehosteten Komponenten ein. Die manifests, die in der Anwendung und in den gehosteten Komponenten enthalten sind, sollten jeweils eine Abhängigkeit von der Assembly beschreiben. In der Regel fügt der Anwendungsentwickler der Anwendung ein Manifest hinzu, und der Entwickler der gehosteten Komponente fügt der DLL, erweiterung, dem Plug-In oder der Systemsteuerung ein Manifest hinzu.

Die folgende Methode kann verwendet werden, um ein Manifest zu einer Anwendung oder einer gehosteten Komponente hinzuzufügen, bei der es sich um eine DLL, erweiterung, ein Plug-In oder eine Systemsteuerung handelt.

**So aktivieren Sie eine Assembly in einer Anwendung oder gehosteten Komponente.**

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

2.  Erstellen Sie eine Ressource in der Anwendung oder Erweiterung des Typs RT \_ MANIFEST ID 2.

    Wenn der Name der Anwendung beispielsweise YourApp ist, sollte die Anwendung Folgendes enthalten:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Kompilieren Sie die Anwendung mit dem Flag -DISOLATION AWARE ENABLED, oder fügen Sie diese Anweisung vor der \_ \_ \# Include-Anweisung "Windows.h" ein. Im Fall einer Anwendung mit mehreren Modulen ist das Flag -DISOLATION \_ AWARE ENABLED für alle Module \_ erforderlich.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Testen Sie , um sicherzustellen, dass assemblys, die von der Anwendung verwendet werden, in der Anwendung und der gehosteten Komponente ordnungsgemäß funktionieren.

Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen ohne Erweiterungen finden Sie unter [Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen.](enabling-an-assembly-in-an-application-without-extensions.md)

 

 



