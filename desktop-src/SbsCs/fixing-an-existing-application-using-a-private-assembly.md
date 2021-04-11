---
description: Ab Windows XP können Sie eine private Assembly erstellen und für eine bestimmte Anwendung verfügbar machen.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Beheben einer vorhandenen Anwendung mit einer privaten Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041672"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Beheben einer vorhandenen Anwendung mit einer privaten Assembly

Ab Windows XP können Sie eine private Assembly erstellen und für eine bestimmte Anwendung verfügbar machen. Diese Funktion kann verwendet werden, um eine Anwendung zu beheben, die mit einem Update nicht kompatibel ist. Ein Beispiel hierfür ist eine Anwendung, die nach dem Upgrade des Betriebssystems nicht mit der neuesten Version von MSVCRT.DLL kompatibel wird. In diesem Fall haben Sie nicht die Möglichkeit, die System Version zu ersetzen, da MSVCRT.DLL eine geschützte Windows-Datei ist. Anstatt die Anwendung für die Verwendung der neuen msvcrt-Version neu schreiben zu müssen, können Sie eine private Assembly für msvcrt erstellen und diese im Anwendungsordner installieren. Beachten Sie, dass nicht jede freigegebene Komponente ein geeigneter Kandidat für eine private parallele Assembly ist, und dass einige Komponenten über Lizenzierungs Einschränkungen verfügen, in denen die Komponenten installiert werden können. Die Komponente muss die Kriterien für eine Seite-an-Seite-Komponente erfüllen. Fragen Sie den Herausgeber der Komponente, wenn Sie eine passende Assembly bereitstellen können.

Das Manifest des private Assembly und das Manifest der Anwendung müssen beide im selben Ordner wie die ausführbare Datei der Anwendung installiert werden. Wenn die Anwendung ausgeführt wird, wird das Anwendungs Manifest konsultiert und die Version von msvcrt geladen, die für die Anwendung privat ist.

In diesem Beispiel enthält die private Assembly sowohl MSVCRT.DLL als auch MSVCIRT.DLL wie im folgenden Assemblymanifest:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

Im folgenden finden Sie ein Beispiel für ein mögliches Anwendungs Manifest.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



