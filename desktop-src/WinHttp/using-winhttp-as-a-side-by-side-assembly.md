---
description: Auf Windows Server 2003 wird WinHTTP als nebeneinander ausgeführte Assembly implementiert und muss als solche verknüpft werden. Beachten Sie, dass dies nicht für Windows Vista und höher gilt.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Verwenden von WinHTTP als nebeneinander ausgeführte Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c6312fb57f210e0324c1ae89bb785fd5b51bcb2b1ea4ba1a4959a3d0fd540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614090"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Verwenden von WinHTTP als nebeneinander ausgeführte Assembly

Auf Windows Server 2003 wird WinHTTP als nebeneinander ausgeführte Assembly implementiert und muss als solche verknüpft werden. Beachten Sie, dass dies nicht für Windows Vista und höher gilt.

## <a name="side-by-side-assemblies"></a>Nebensassemblys

Ab Microsoft Windows XP wurde ein mechanismus für nebeneinander ausgeführte Assemblys bereitgestellt, um die Laufzeitverknüpfung zu steuern, um Dll-Versionskonflikte (Dynamic Link Library) zu vermeiden. Informationen zu nebenseitigen Assemblys finden Sie unter [Informationen zu isolierten Anwendungen und nebenseitigen Assemblys.](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)

Um diesen Mechanismus zum Verknüpfen mit WinHTTP Version 5.1 auf Windows Server 2003 zu verwenden, muss eine Anwendung ein Manifest enthalten, das WinHTTP als abhängige Assembly angibt. Weitere Informationen hierzu finden Sie unter Verwenden von [nebenseitigen Assemblys.](/windows/desktop/SbsCs/using-side-by-side-assemblies)

## <a name="a-sample-winhttp-application-manifest"></a>Ein WinHTTP-Beispielanwendungsmanifest

Das folgende Beispielmanifest veranschaulicht ein Anwendungsmanifest, das zum Verknüpfen mit WinHTTP verwendet werden kann.

Alle Attribute außer dem "Typ" von <assembly> <assemblyIdentity> "" müssen entsprechend Ihrer jeweiligen Anwendung geändert werden. Dasselbe gilt für den Inhalt des &lt; &gt; "description"-Elements.

Stellen Sie außerdem sicher, dass das "processorArchitecture"-Attribut von <dependentAssembly> <assemblyIdentity> " " mit dem "processorArchitecture"-Attribut von "" <assembly> <assemblyIdentity> übereinstimmt. Unten sind beispielsweise beide auf "x86" festgelegt.

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

 

 
