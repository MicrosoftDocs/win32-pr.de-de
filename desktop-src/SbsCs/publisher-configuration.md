---
description: Eine Verleger Konfigurationsdatei leitet Anwendungen und Assemblys mit Abhängigkeit von einer Version einer parallelen Assembly Global um, um eine andere Version derselben Assembly zu verwenden.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Herausgeber Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217793"
---
# <a name="publisher-configuration"></a>Herausgeber Konfiguration

Eine [Verleger Konfigurationsdatei](publisher-configuration-files.md) leitet Anwendungen und Assemblys mit Abhängigkeit von einer Version einer parallelen Assembly Global um, um eine andere Version derselben Assembly zu verwenden. Dies ermöglicht es Anwendungen und Assemblys, die aktualisierte Assembly zu verwenden, ohne alle betroffenen Anwendungen neu erstellen zu müssen.

Die [Verleger Konfigurationsdateien](publisher-configuration-files.md) können vom Verleger einer Assembly bereitgestellt werden, wenn eine neue Version der Assembly mit kompatiblen Fehlerbehebungen oder Sicherheitsupdates ausgegeben wird. Die aktualisierte Version sollte vollständig abwärts kompatibel sein. Eine Verleger Konfigurationsdatei sollte nie zum Hinzufügen neuer Features verwendet werden, es sei denn, das Update ist vollständig abwärts kompatibel. Die Verleger Konfigurationsdateien sollten niemals verwendet werden, um die Haupt-oder neben Version einer Assembly zu erhöhen. Umleiten Sie z. b. die Assemblyversion 6.0.0.0 nicht an 7.0.0.0 oder 6.1.0.0.

Die Verleger Konfigurationsdateien sollten nur vom Verleger der Assembly ausgestellt werden. Assemblyentwickler sollten freigegebene parallele Assemblys und Verleger Konfigurationsdateien signieren. Verwenden Sie den gleichen Schlüssel, um die Assembly und die zugehörigen Verleger Konfigurationsdateien zu signieren. Die Verleger Konfigurationsdateien sollten mithilfe der gleichen Tools wie für Assemblys signiert werden. Informationen hierzu finden Sie unter [Beispiel für Assemblysignierung](assembly-signing-example.md) und [Erstellen signierter Dateien](creating-signed-files-and-catalogs.md)

In der Regel werden die neue Version einer Assembly und die zugehörige Verleger Konfigurationsdatei in einem Service Pack Update installiert. Die Verleger Konfigurationsdateien sollten nie als verteilbare Anwendungen mit Anwendungen bereitgestellt werden, da die Installation einer Verleger Konfigurationsdatei die Assemblys auf dem System Global umleitet. Wenn die zu Aktualisier Ende Assembly als verteilbare Komponente bereitgestellt wird, sollte der Herausgeber beide der folgenden Optionen bereitstellen.

-   Ein Windows Installer Paket (MSI-Datei), das die neue Version der Assembly mit der Verleger Konfiguration enthält. Dies kann als Service Pack oder QFE installiert werden, da der Kunde in diesem Fall das System global aktualisieren möchte. Diese Version des Pakets sollte nie von Anwendungen installiert werden.
-   Ein Windows Installer Mergemodul (MSM-Datei), das nur die neue Version der Assembly enthält. Diese Version ist möglicherweise in-Anwendungen enthalten.

Anwendungen, die eine Mindestversion der Assembly benötigen, sollten ihre Abhängigkeit von der Mindestversion angeben. wenn die Mindestversion auf einem System nicht verfügbar ist, kann die Anwendung nicht gestartet werden. Wenn Sie als verteilbare Komponente verfügbar ist, sollte Sie in das Setup der Anwendung eingeschlossen werden.

Wenn Sie beispielsweise die folgende [Verleger Konfigurationsdatei](publisher-configuration-files.md) installieren, wird die Bindung von Version 2.0.0.0 von Microsoft. Windows. SampleAssembly an Version 2.0.1.0 umgeleitet. Dadurch wird eine neue Richtlinie mit dem Namen 1.1.0.0. Policy unter% System Drive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*> hinzugefügt.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

Wenn Sie die folgende Verleger Konfigurationsdatei für dieselbe Assembly installieren, wird die Bindung von der 2.0.0.0-Version von Microsoft. Windows. SampleAssembly an Version 2.0.3.0 umgeleitet. Dadurch wird eine weitere Richtlinie mit dem Namen 2.1.0.0. Policy unter% System Drive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*> hinzugefügt.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



