---
description: Auf Windows XP überschreibt die Konfiguration pro Anwendung sowohl die Standardkonfiguration als auch die Herausgeberkonfiguration pro Anwendung.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Anwendungsspezifische Konfiguration auf Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f07860a42951e073403e8145037074c35e6ec6a267736381f6beab385f3bb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127460"
---
# <a name="per-application-configuration-on-windows-xp"></a>Anwendungsspezifische Konfiguration auf Windows XP

Auf Windows XP überschreibt die Konfiguration pro Anwendung sowohl die [Standardkonfiguration](default-configuration.md) als auch die [Herausgeberkonfiguration](publisher-configuration.md) pro Anwendung. Dadurch wird die Abhängigkeit einer bestimmten Anwendung von einer Version einer side-by-side-Assembly zu einer anderen angegebenen Version der Assembly umgeleitet.

> [!Note]  
> Ab Windows Server 2003 überschreibt die Anwendungskonfiguration die [Herausgeberkonfiguration](publisher-configuration.md) nur dann auf Anwendungsbasis, wenn die [Anwendungskonfigurationsdatei](application-configuration-files.md) *apply="no"* in **publisherPolicy** angibt und ein entsprechender Eintrag in der Anwendungskompatibilitätsdatenbank vorhanden ist. Die Konfiguration pro Anwendung überschreibt immer die [Standardkonfiguration](default-configuration.md). Weitere Informationen finden Sie unter [Anwendungsspezifische Konfiguration.](per-application-configuration.md)

 

Eine Anwendungsspezifische Konfiguration kann erforderlich werden, wenn für den richtigen Betrieb einer bestimmten Anwendung eine Assemblyversion erforderlich ist, die sich von der Version unterscheidet, die normalerweise als Standard- oder Herausgeberkonfiguration angegeben ist. Beispielsweise kann ein globales Update der Assemblyversion durch den Herausgeber die Assembly korrigieren, aber diese bestimmte Anwendung unterbrechen. In diesem Fall kann die Anwendungskonfiguration verwendet werden, damit die Anwendung weiterhin mit der vorherigen Assemblyversion ausgeführt werden kann. Ein weiteres Beispiel: Eine Service Pack-Installation, die ein Assemblyupdate enthält, kann die [Herausgeberkonfiguration](publisher-configuration.md) verwenden, um die Abhängigkeiten aller Anwendungen und Assemblys auf dem System von Version 1.0.0.0 auf 1.0.1.0 umzuleiten. Wenn es eine Anwendung gibt, die erfordert, dass Version 1.0.0.0 ordnungsgemäß funktioniert, kann sie mithilfe der Anwendungskonfiguration auf Version 1.0.0.0 umgeleitet werden.

Anwendungsadministratoren können eine Anwendungskonfiguration implementieren, indem sie [Anwendungskonfigurationsdateien](application-configuration-files.md)erstellen und installieren. Diese leiten eine bestimmte Anwendung von einer Abhängigkeit von einer Version einer nebeneinander ausgeführten Assembly in Abhängigkeit von einer anderen Version um. [*Anwendungskonfigurationsdateien*](/windows/desktop/Msi/a-gly) können [Herausgeberkonfigurationsdateien](publisher-configuration-files.md) und die durch [Anwendungsmanifeste](application-manifests.md) und [Assemblymanifeste](assembly-manifests.md)angegebene Standardkonfiguration außer Kraft setzen. Die Anwendungskonfigurationsdatei enthält Informationen, die vom Ladeprogramm beim Aufruf von [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) verwendet werden.

Um eine Anwendung so zu konfigurieren, dass sie sowohl das Anwendungsmanifest als auch die Herausgeberkonfiguration außer Kraft setzt, muss ein Entwickler eine Anwendungskonfigurationsdatei erstellen. Die Anwendungskonfigurationsdatei wird dann bereitgestellt und in demselben Ordner wie die ausführbare Datei der Anwendung installiert. Eine Liste des Dateischemas finden Sie unter [Anwendungskonfigurationsdateischema.](application-configuration-file-schema.md)

Beachten Sie Folgendes: Wenn Ihre Anwendung anwendungsspezifische Konfigurationen verwendet, erhält sie keine wichtigen Sicherheitskorrekturen oder Fehlerbehebungen, die der Herausgeber der Assembly möglicherweise als Herausgeberkonfigurationsdateien ausstellt. Eine Anwendung, die anwendungsspezifische Konfigurationen verwendet, bleibt daher möglicherweise unsicher oder funktioniert auch dann nicht ordnungsgemäß, wenn eine neue Assembly mit diesen Fehlerbehebungen auf das System angewendet wurde. Aus diesem Grund sollten Anwendungsentwickler niemals eine Anwendung mit einer Anwendungskonfiguration versenden. Die Anwendungsspezifische Konfiguration sollte nur von Unternehmensadministratoren als temporäre Korrektur verwendet werden, wenn die Anwendung durch eine Herausgeberkonfiguration beschädigt wird. In diesem Fall besteht die dauerhafte Lösung darin, dass die Entwickler der Assembly und die Entwickler der Anwendung zusammenarbeiten müssen, um sicherzustellen, dass die Assemblys mit der Herausgeberkonfiguration vollständig abwärtskompatibel sind.

Im Folgenden wird ein Beispiel für eine Anwendungskonfigurationsdatei angezeigt. Weitere Informationen finden Sie unter [Anwendungskonfigurationsdateien.](application-configuration-files.md)

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

 

 
