---
description: Im folgenden Beispiel wird erläutert, wie eine signierte side-by-side-Assembly generiert wird, die aus dem Assemblymanifest, dem Überprüfungskatalog und den Assemblydateien besteht.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Beispiel für die Assemblysignierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896da43b846edfd09348c6515fbf5e44fdd45dd2911b9fcdcf25e99f63fb6ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142463"
---
# <a name="assembly-signing-example"></a>Beispiel für die Assemblysignierung

Im folgenden Beispiel wird erläutert, wie eine signierte side-by-side-Assembly generiert wird, die aus dem Assemblymanifest, dem Überprüfungskatalog und den Assemblydateien besteht. Freigegebene nebeneinander verwendete Assemblys sollten signiert werden. Das Betriebssystem überprüft die Assemblysignatur, bevor eine freigegebene Assembly im globalen side-by-side-Speicher (WinSxS) installiert wird. Dies erschwert das Spoofing des Herausgebers der nebeneinanderseitigen Assembly.

Beachten Sie, dass das Ändern der Assemblydateien oder des Manifestinhalts nach dem Generieren des Assemblykatalogs den Katalog und die Assembly ungültig macht. Wenn Sie die Assemblydateien oder das Manifest nach dem Erstellen und Signieren des Katalogs aktualisieren müssen, müssen Sie die Assembly erneut signieren und einen neuen Katalog generieren.

Beginnen Sie mit den Assemblydateien, dem Assemblymanifest und der Zertifikatdatei, die Sie zum Signieren der Assembly verwenden. Die Zertifikatdatei muss 2048 Bit oder größer sein. Sie müssen kein vertrauenswürdiges Zertifikat verwenden. Das Zertifikat wird nur verwendet, um zu überprüfen, ob die Assembly nicht beschädigt wurde.

Führen Sie das [hilfsprogrammPktextract.exe](pktextract-exe.md) aus, das im Microsoft Windows Software Development Kit (SDK) bereitgestellt wird, um das öffentliche Schlüsseltoken aus der Zertifikatdatei zu extrahieren. Damit Pktextract ordnungsgemäß funktioniert, muss die Zertifikatdatei im selben Verzeichnis wie das Hilfsprogramm vorhanden sein. Verwenden Sie den extrahierten Tokenwert des öffentlichen Schlüssels, um das **publicKeyToken-Attribut** des **assemblyIdentity-Elements** in der Manifestdatei zu aktualisieren.

Hier sehen Sie ein Beispiel für eine Manifestdatei mit dem Namen MySampleAssembly.manifest. Die MySampleAssembly-Assembly enthält nur eine Datei, MYFILE.DLL. Beachten Sie, dass der Wert für das **publicKeyToken-Attribut** des **assemblyIdentity-Elements** mit dem Wert des öffentlichen Schlüsseltokens aktualisiert wurde.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

Führen Sie als Nächstes das [hilfsprogrammMt.exe](mt-exe.md) aus, das im Windows SDK bereitgestellt wird. Die Assemblydateien müssen sich im gleichen Verzeichnis wie das Manifest befinden. In diesem Beispiel ist dies das Verzeichnis MySampleAssembly. Rufen Sie Mt.exe für das Beispiel wie folgt auf:

**c: \\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**

Das Beispielmanifest sieht wie folgt aus, nachdem Mt.exe ausgeführt wurde. Beachten Sie, dass die Ausführung von Mt.exe mit der Hashupdateoption den SHA-1-Hash der Datei hinzufügt. Ändern Sie diesen Wert nicht.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

Wenn Sie Mt.exe mit der Option -makecdfs ausführen, wird eine Datei mit dem Namen MySampleAssembly.manifest.cdf generiert, die den Inhalt des Sicherheitskatalogs beschreibt, der zum Überprüfen des Manifests verwendet wird.

Der nächste Schritt besteht darin, Makecat.exe über diese CDF-Datei auszuführen, um den Sicherheitskatalog für die Assembly zu erstellen. Der Aufruf von Makecat.exe für dieses Beispiel würde wie folgt aussehen:

**c: \\ MySampleAssembly>Makecat MySampleAssembly.manifest.cdf**

Der letzte Schritt besteht darin, SignTool.exe auszuführen, um die Katalogdatei mit dem Zertifikat zu signieren. Dies sollte dasselbe Zertifikat sein, das im vorherigen zum Generieren des öffentlichen Schlüsseltokens verwendet wurde. Weitere Informationen zu SignTool.exe finden Sie im Thema [**SignTool.**](../seccrypto/signtool.md) Der Aufruf von **SignTool** für das Beispiel würde wie folgt aussehen:

**c: \\ MySampleAssembly>signtool sign /f \<fullpath> mycompany.pfx /du https: \/ /www.mycompany.com/MySampleAssembly /t https: \/ /timestamp.digicert.com MySampleAssembly.cat**

Wenn Sie über ein authentifiziertes digitales Zertifikat verfügen und Ihre Zertifizierungsstelle das PVK-Dateiformat zum Speichern des privaten Schlüssels verwendet, können Sie den PvK Digital Certificate Files Importer (pvkimprt.exe) verwenden, um den Schlüssel in Ihren Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) zu importieren. Mit diesem Hilfsprogramm können Sie das Branchenstandardformat PFX/P12 exportieren. Weitere Informationen zum PVK Digital Certificate Files Importer finden Sie im Abschnitt Bereitstellungsressourcen der MSDN-Bibliothek, oder wenden Sie sich an Ihre Zertifizierungsstelle. Möglicherweise können Sie pvkimprt.exe von https://office.microsoft.com/downloads/2000/pvkimprt.aspx abrufen.

Siehe auch [Erstellen von signierten Dateien und Katalogen.](creating-signed-files-and-catalogs.md)

 

 
