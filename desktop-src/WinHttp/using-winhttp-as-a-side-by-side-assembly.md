---
description: Unter Windows Server 2003 wird WinHTTP als parallele Assembly implementiert und muss als solche verknüpft werden. Beachten Sie, dass dies nicht für Windows Vista und höher gilt.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Verwenden von WinHTTP als parallele Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751512"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Verwenden von WinHTTP als parallele Assembly

Unter Windows Server 2003 wird WinHTTP als parallele Assembly implementiert und muss als solche verknüpft werden. Beachten Sie, dass dies nicht für Windows Vista und höher gilt.

## <a name="side-by-side-assemblies"></a>Parallele Assemblys

Ab Microsoft Windows XP wurde ein paralleler assemblymechanismus bereitgestellt, um die Lauf Zeit Verknüpfung zu steuern und Konflikte mit der dll (Dynamic Link Library) zu vermeiden. Weitere Informationen zu parallelen Assemblys finden Sie unter Informationen [zu isolierten Anwendungen und](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)parallelen Assemblys.

Um diesen Mechanismus zum Verknüpfen mit WinHTTP-Version 5,1 unter Windows Server 2003 zu verwenden, muss eine Anwendung ein Manifest einschließen, das WinHTTP als abhängige Assembly angibt. Weitere Informationen hierzu finden Sie unter [verwenden](/windows/desktop/SbsCs/using-side-by-side-assemblies) paralleler Assemblys.

## <a name="a-sample-winhttp-application-manifest"></a>Ein WinHTTP-Beispiel Anwendungs Manifest

Das folgende Beispiel Manifest veranschaulicht ein Anwendungs Manifest, das zum Verknüpfen mit WinHTTP verwendet werden kann.

Alle Attribute außer "Type" von " <assembly> <assemblyIdentity> " müssen entsprechend Ihren Anwendungen geändert werden. Das gleiche gilt für den Inhalt des " &lt; Description &gt; "-Elements.

Stellen Sie außerdem sicher, dass das Attribut "ProcessorArchitecture" von " <dependentAssembly> <assemblyIdentity> " mit dem Attribut "ProcessorArchitecture" von "" übereinstimmt <assembly> <assemblyIdentity> . Im folgenden Beispiel werden beide auf "x86" festgelegt.

Alle Werte, die nicht spezifisch für Ihre Anwendung sind, sollten die unten gezeigten Formen annehmen.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
