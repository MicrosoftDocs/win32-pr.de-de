---
description: Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, um die parallelen Assemblys zu verwenden, die von Microsoft oder anderen parallelen assemblyverlegern verfügbar sind.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Verwenden paralleler Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862331"
---
# <a name="using-side-by-side-assemblies"></a>Verwenden paralleler Assemblys

Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, [um die parallelen](about-side-by-side-assemblies-.md) Assemblys zu verwenden, die von Microsoft oder anderen parallelen assemblyverlegern verfügbar sind. Eine Liste der parallelen Assemblys, die derzeit von Microsoft bereitgestellt werden, finden Sie [unter Unterstützte](supported-microsoft-side-by-side-assemblies.md)parallele Assemblys von Microsoft. Beachten Sie, dass die Anwendung auf mindestens Windows XP ausgeführt werden muss, um die Assemblys als parallele Assemblys zu installieren. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.

**So fügen Sie einer Anwendung eine Seite-an-Seite-Assembly hinzu**

1.  Identifizieren Sie die parallelen Assemblys, die für die Anwendung erforderlich sind. Ab Windows XP werden diese parallelen Assemblys und ihre Assemblymanifeste mit dem Betriebssystem installiert, aber nicht global registriert.
2.  Verwenden Sie einen XML-Editor, um ein [Anwendungs Manifest](application-manifests.md)zu erstellen. Weitere Informationen finden Sie unten im Beispiel Anwendungs Manifest. Weitere Informationen finden Sie unter [Anwendungs Manifeste](application-manifests.md) in der [Manifest-Dateireferenz](manifest-files-reference.md).
3.  Geben Sie die Attributwerte im [*DEF-Context-Unterelement assemblyIdentity*](d-sbscs-gly.md) des Anwendungs Manifests ein, das die Anwendung eindeutig definiert. Weitere Informationen zum DEF-Kontext **assemblyIdentity** finden Sie unter [Anwendungs Manifeste](application-manifests.md).
4.  Wenn die Assembly abhängige Assemblys enthält, geben Sie Attributwerte in die entsprechenden untergeordneten Elemente der [*ref-Context-Assemblyidentität*](r-sbscs-gly.md) des Anwendungs Manifests ein. Weitere Informationen zum Verweis Kontext **assemblyIdentity** finden Sie unter [Anwendungs Manifeste](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Sie können das Anwendungs Manifest in die binäre ausführbare Header Datei der Anwendung einschließen.

    Fügen Sie in diesem Fall auch die folgende Zeile zur Anwendungs Header Datei hinzu:

    <dl> Die Ressourcen- \_ \_ ID RT-Manifest der Ressourcen- \_ ID RT \_ "YourApp.exe. Manifest".  
    </dl>

    Als Alternative können Sie eine separate Manifest-Datei im gleichen Verzeichnis wie die ausführbare Datei der Anwendung platzieren. Das Betriebssystem lädt das Manifest zuerst aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei. Die Dateisystem Version hat Vorrang.

6.  Frei [gegebene](/windows/desktop/Msi/shared-assemblies) Assemblys sollten mit dem [Windows Installer](../msi/windows-installer-portal.md) Version 2,0 installiert werden. Erstellen Sie ein Windows Installer Paket, wie unter Gewusst wie: Installieren von Win32-Assemblys für die parallele [Freigabe unter Windows XP](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)beschrieben.
7.  [Private](/windows/desktop/Msi/private-assemblies) Assemblys können mit der [Windows Installer](../msi/windows-installer-portal.md) Version 2,0 installiert werden. Erstellen Sie ein Windows Installer Paket, wie unter Gewusst wie: Installieren von Win32-Assemblys [für die private Verwendung einer Anwendung unter Windows XP](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)beschrieben. Sie können auch ein beliebiges anderes Installationsprogramm verwenden, um eine private Assembly und das zugehörige Manifest in denselben Ordner wie die ausführbare Datei der Anwendung zu kopieren.
8.  Testen Sie Ihre Anwendung, um die Ergebnisse sicherzustellen. Beachten Sie, dass auf dem Testcomputer nicht die parallele Assembly registriert sein sollte.
9.  Stellen Sie die Anwendung bereit, oder aktualisieren Sie Sie als Windows Installer Paket.

## <a name="example-application-manifest"></a>Beispiel für ein Anwendungs Manifest

Im folgenden finden Sie ein Beispiel für ein Anwendungs Manifest:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
