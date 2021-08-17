---
description: Eine Herausgeberkonfigurationsdatei leitet Anwendungen und Assemblys global um, die von einer Version einer parallelen Assembly abhängig sind, um eine andere Version derselben Assembly zu verwenden.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Publisher Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1134fa29775fc34384f5da19e660d91de10532110304caf8b6ecacbb92fec87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141953"
---
# <a name="publisher-configuration"></a>Publisher Konfiguration

Eine [Herausgeberkonfigurationsdatei](publisher-configuration-files.md) leitet Anwendungen und Assemblys global um, die von einer Version einer parallelen Assembly abhängig sind, um eine andere Version derselben Assembly zu verwenden. Dadurch können Anwendungen und Assemblys die aktualisierte Assembly verwenden, ohne alle betroffenen Anwendungen neu erstellen zu müssen.

[Publisher Konfigurationsdateien](publisher-configuration-files.md) können vom Herausgeber einer Assembly bereitgestellt werden, wenn eine neue Version der Assembly mit kompatiblen Fehlerbehebungen oder Sicherheitsupdates ausgegeben wird. Die aktualisierte Version sollte vollständig abwärtskompatibel sein. Eine Herausgeberkonfigurationsdatei sollte niemals verwendet werden, um neue Features hinzuzufügen, es sei denn, das Update ist vollständig abwärtskompatibel. Publisher Konfigurationsdateien sollten nie verwendet werden, um die Haupt- oder Nebenversion einer Assembly zu erhöhen. Leiten Sie beispielsweise Assemblyversion 6.0.0.0 nicht zu 7.0.0.0 oder 6.1.0.0 um.

Publisher Konfigurationsdateien sollten nur vom Herausgeber der Assembly ausgegeben werden. Assemblyentwickler sollten freigegebene nebeneinander verwendete Assemblys und Herausgeberkonfigurationsdateien signieren. Verwenden Sie den gleichen Schlüssel, um die Assembly und die zugehörigen Herausgeberkonfigurationsdateien zu signieren. Publisher Konfigurationsdateien mit den gleichen Tools signiert werden sollten, die auch für Assemblys verwendet werden, finden Sie unter [AssemblySignierungsbeispiel](assembly-signing-example.md) und [Erstellen von signierten Dateien und Katalogen.](creating-signed-files-and-catalogs.md)

In der Regel werden die neue Version einer Assembly und die zugehörige Herausgeberkonfigurationsdatei in einem Service Pack-Update installiert. Publisher Konfigurationsdateien sollten niemals mit Anwendungen als weitervertreverteilbar bereitgestellt werden, da durch die Installation einer Herausgeberkonfigurationsdatei Assemblys global auf dem System umgeleitet werden. Wenn die zu aktualisierende Assembly als verteilbare Assembly bereitgestellt wird, sollte der Herausgeber beides bereitstellen:

-   Ein Windows Installer-Paket (.msi-Datei), das die neue Version der Assembly mit Herausgeberkonfiguration enthält. Dies kann als Service Pack oder QFE installiert werden, da sich der Kunde in diesem Fall für eine globale Aktualisierung des Systems entschieden hat. Diese Version des Pakets sollte nie von Anwendungen installiert werden.
-   Ein Windows Installer-Mergemodul (MSM-Datei), das nur die neue Version der Assembly enthält. Diese Version kann in Anwendungen enthalten sein.

Anwendungen, die eine Mindestversion der Assembly erfordern, sollten ihre Abhängigkeit von der Mindestversion aufweisen. Wenn die Mindestversion auf einem System nicht verfügbar ist, kann die Anwendung nicht gestartet werden. Wenn sie als weitervertrendbar verfügbar ist, sollte sie in das Anwendungssetup aufgenommen werden.

Wenn Sie beispielsweise die folgende [Herausgeberkonfigurationsdatei](publisher-configuration-files.md) installieren, wird die Bindung von Version 2.0.0.0 von Microsoft umgeleitet. Windows. SampleAssembly auf Version 2.0.1.0. Dadurch wird unter %systemDrive% windows winsxs policies x86 policy.2.0.Microsoft.Windows eine neue Richtlinie mit dem Namen \\ \\ \\ \\ \_ 1.1.0.0.Policy hinzugefügt. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

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

Wenn Sie die folgende Herausgeberkonfigurationsdatei für dieselbe Assembly installieren, wird die Bindung von Version 2.0.0.0 von Microsoft umgeleitet. Windows. SampleAssembly auf Version 2.0.3.0. Dadurch wird unter %systemDrive% windows winsxs policies x86 policy.2.0.Microsoft.Windows eine weitere Richtlinie mit dem Namen \\ \\ \\ \\ \_ 2.1.0.0.Policy hinzugefügt. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

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

 

 



