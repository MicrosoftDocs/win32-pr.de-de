---
description: Unter Windows XP überschreibt die Konfiguration pro Anwendung sowohl die Standardkonfiguration als auch die Verleger Konfiguration pro Anwendung.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Konfiguration pro Anwendung unter Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867895"
---
# <a name="per-application-configuration-on-windows-xp"></a>Konfiguration pro Anwendung unter Windows XP

Unter Windows XP überschreibt die Konfiguration pro Anwendung sowohl die [Standardkonfiguration](default-configuration.md) als auch die [Verleger Konfiguration](publisher-configuration.md) pro Anwendung. Dadurch wird die Abhängigkeit einer bestimmten Anwendung von einer Version einer parallelen Assembly zu einer anderen angegebenen Version der Assembly umgeleitet.

> [!Note]  
> Ab Windows Server 2003 überschreibt die Konfiguration pro Anwendung nur die [Verleger Konfiguration](publisher-configuration.md) pro Anwendung, wenn in der [Anwendungs Konfigurationsdatei](application-configuration-files.md) *Apply = "No"* in **publisherPolicy** angegeben wird und ein entsprechender Eintrag in der Anwendungskompatibilitäts-Datenbank vorhanden ist. Die Konfiguration pro Anwendung überschreibt immer die [Standardkonfiguration](default-configuration.md). Weitere Informationen finden Sie unter [Konfiguration pro Anwendung](per-application-configuration.md).

 

Eine Konfiguration pro Anwendung ist möglicherweise erforderlich, wenn der korrekte Betrieb einer bestimmten Anwendung eine Assemblyversion erfordert, die sich von der normalerweise als Standard-oder Verleger Konfiguration angegebenen Version unterscheidet. Beispielsweise kann ein globales Update der Assemblyversion durch den Verleger die Assembly beheben, diese spezielle Anwendung jedoch unterbrechen. In diesem Fall kann die Konfiguration pro Anwendung verwendet werden, damit die Anwendung weiterhin mit der vorherigen Assemblyversion ausgeführt werden kann. Ein weiteres Beispiel: bei einer Service Pack Installation mit einem assemblyupdate kann die [Herausgeber Konfiguration](publisher-configuration.md) verwendet werden, um die Abhängigkeiten aller Anwendungen und Assemblys auf dem System von Version 1.0.0.0 zu 1.0.1.0 umzuleiten. Wenn eine Anwendung, die Version 1.0.0.0 erfordert, ordnungsgemäß funktioniert, kann Sie mithilfe der Konfiguration pro Anwendung an Version 1.0.0.0 umgeleitet werden.

Anwendungs Administratoren können eine Konfiguration pro Anwendung implementieren, indem Sie [Anwendungs Konfigurationsdateien](application-configuration-files.md)erstellen und installieren. Diese leiten eine bestimmte Anwendung von der Abhängigkeit von einer Version einer parallelen Assembly in Abhängigkeit von einer anderen Version um. [*Anwendungs Konfigurationsdateien*](/windows/desktop/Msi/a-gly) können die [Verleger Konfigurationsdateien](publisher-configuration-files.md) und die von [Anwendungs Manifesten](application-manifests.md) und Assemblymanifesten angegebene Standardkonfiguration überschreiben. [](assembly-manifests.md) Die Anwendungs Konfigurationsdatei enthält Informationen, die vom Lade Modul verwendet werden, wenn " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " aufgerufen wird.

Um eine Anwendung so zu konfigurieren, dass sowohl das Anwendungs Manifest als auch die Verleger Konfiguration außer Kraft gesetzt wird, muss ein Entwickler eine Anwendungs Konfigurationsdatei erstellen. Die Anwendungs Konfigurationsdatei wird dann im selben Ordner wie die ausführbare Datei der Anwendung bereitgestellt und installiert. Eine Auflistung des Datei Schemas finden Sie unter [Schema der Anwendungs Konfigurationsdatei](application-configuration-file-schema.md).

Beachten Sie Folgendes: Wenn Ihre Anwendung anwendungsspezifische Konfigurationen verwendet, erhalten Sie keine wichtigen Sicherheitskorrekturen oder Fehlerbehebungen, die der Herausgeber der Assembly als Verleger Konfigurationsdateien ausgeben kann. Eine Anwendung, die die Konfiguration pro Anwendung verwendet, ist daher möglicherweise unsicher oder auch nach dem Anwenden einer neuen Assembly mit diesen Korrekturen auf das System weiterhin fehlerhaft. Aus diesem Grund sollten Anwendungsentwickler niemals eine Anwendung mit einer Konfiguration pro Anwendung versenden. Die Konfiguration pro Anwendung sollte nur von Unternehmens Administratoren als temporäre Korrektur verwendet werden, wenn die Anwendung durch eine Verleger Konfiguration beschädigt ist. In diesem Fall besteht die permanente Lösung darin, dass die Entwickler der Assembly und die Entwickler der Anwendung zusammenarbeiten müssen, um sicherzustellen, dass die Assemblys mit der Verleger Konfiguration vollständig abwärts kompatibel sind.

Im folgenden finden Sie ein Beispiel für eine Anwendungs Konfigurationsdatei. Weitere Informationen finden Sie unter [Anwendungs Konfigurationsdateien](application-configuration-files.md).

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
