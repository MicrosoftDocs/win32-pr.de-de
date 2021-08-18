---
description: Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, um die von Microsoft oder anderen verlegern für nebeneinander verfügbare Assemblys zu verwenden.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Verwenden von nebeneinander ausgeführten Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141713"
---
# <a name="using-side-by-side-assemblies"></a>Verwenden von nebeneinander ausgeführten Assemblys

Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, um die von Microsoft oder anderen verlegern für nebeneinander verfügbare [Assemblys](about-side-by-side-assemblies-.md) zu verwenden. Eine Liste der zurzeit von Microsoft bereitgestellten nebenseitigen Assemblys finden Sie unter [Unterstützte microsoftseitige Assemblys.](supported-microsoft-side-by-side-assemblies.md) Beachten Sie, dass die Anwendung auf mindestens Windows XP ausgeführt werden muss, um die Assemblys als nebeneinander ausgeführte Assemblys zu installieren. Weitere Informationen finden Sie unter [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).

**So fügen Sie einer Anwendung eine side-by-side-Assembly hinzu**

1.  Identifizieren Sie die von der Anwendung benötigten nebenseitigen Assemblys. Ab Windows XP werden diese assemblys und ihre Assemblymanifeste mit dem Betriebssystem installiert, aber nicht global registriert.
2.  Verwenden Sie einen XML-Editor, um ein [Anwendungsmanifest](application-manifests.md)zu erstellen. Weitere Informationen finden Sie unten im Beispielanwendungsmanifest. Weitere Informationen finden Sie unter [Anwendungsmanifeste](application-manifests.md) in der [Manifestdateienreferenz.](manifest-files-reference.md)
3.  Geben Sie Attributwerte im [*DEF-KontextassemblyIdentity-Unterelement*](d-sbscs-gly.md) des Anwendungsmanifests ein, das die Anwendung eindeutig definiert. Weitere Informationen zur **DEF-KontextassemblyIdentity** finden Sie unter [Anwendungsmanifeste.](application-manifests.md)
4.  Wenn die Assembly abhängige Assemblys enthält, geben Sie Attributwerte in die entsprechenden [*ASSEMBLYIdentity-Unterelemente im REF-Kontext*](r-sbscs-gly.md) des Anwendungsmanifests ein. Weitere Informationen zur **REF-KontextassemblyIdentity** finden Sie unter [Anwendungsmanifeste.](application-manifests.md)

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Sie können das Anwendungsmanifest in die binäre ausführbare Headerdatei der Anwendung einschließen.

    Fügen Sie in diesem Fall auch die folgende Zeile zur Anwendungsheaderdatei hinzu:

    <dl> CREATEPROCESS \_ MANIFEST RESOURCE ID RT MANIFEST \_ \_ \_ "YourApp.exe.manifest"  
    </dl>

    Alternativ können Sie eine separate Manifestdatei im selben Verzeichnis wie die ausführbare Datei Ihrer Anwendung platzieren. Das Betriebssystem lädt zuerst das Manifest aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei. Die Dateisystemversion hat Vorrang.

6.  [Freigegebene Assemblys](/windows/desktop/Msi/shared-assemblies) sollten mit dem [Windows Installer](../msi/windows-installer-portal.md) Version 2.0 installiert werden. Erstellen Sie ein Windows Installer-Paket, wie unter [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP? (Installieren von Win32-Assemblys für die parallele Freigabe auf Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)beschrieben).
7.  [Private Assemblys](/windows/desktop/Msi/private-assemblies) können mit dem [Windows Installer](../msi/windows-installer-portal.md) Version 2.0 installiert werden. Erstellen Sie ein Windows Installer-Paket, wie unter [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP? (Wie installiere ich Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP?)](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)beschrieben. Sie können auch ein beliebiges anderes Installationsprogramm verwenden, um eine private Assembly und ihr Manifest in denselben Ordner wie die ausführbare Datei der Anwendung zu kopieren.
8.  Testen Sie Ihre Anwendung, um die Ergebnisse sicherzustellen. Beachten Sie, dass auf dem Testcomputer die side-by-side-Assembly nicht registriert sein sollte.
9.  Stellen Sie Ihre Anwendung bereit, oder aktualisieren Sie sie als Windows Installer-Paket.

## <a name="example-application-manifest"></a>Beispielanwendungsmanifest

Es folgt ein Beispiel für ein Anwendungsmanifest:

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

 

 
