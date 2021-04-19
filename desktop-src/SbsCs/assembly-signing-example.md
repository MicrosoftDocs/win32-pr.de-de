---
description: Im folgenden Beispiel wird erläutert, wie eine signierte parallele Assembly generiert wird, die aus dem Assemblymanifest, dem Überprüfungs Katalog und den Assemblydateien besteht.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Beispiel für die Assemblysignierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106355777"
---
# <a name="assembly-signing-example"></a>Beispiel für die Assemblysignierung

Im folgenden Beispiel wird erläutert, wie eine signierte parallele Assembly generiert wird, die aus dem Assemblymanifest, dem Überprüfungs Katalog und den Assemblydateien besteht. Freigegebene parallele Assemblys sollten signiert werden. Das Betriebssystem überprüft die Assemblysignatur vor der Installation einer freigegebenen Assembly im globalen parallelen Speicher (WinSxS). Dadurch wird es schwierig, den Herausgeber der Seite-an-Seite-Assembly zu spoomachen.

Beachten Sie, dass das Ändern der Assemblydateien oder der Inhalt des Manifests nach der Erstellung des assemblykatalogs den Katalog und die Assembly für ungültig erklärt. Wenn Sie die Assemblydateien oder das Manifest nach dem Erstellen und Signieren des Katalogs aktualisieren müssen, müssen Sie die Assembly erneut signieren und einen neuen Katalog generieren.

Beginnen Sie mit den Assemblydateien, dem Assemblymanifest und der Zertifikatsdatei, die Sie zum Signieren der Assembly verwenden. Die Zertifikatsdatei muss 2048 Bit oder größer sein. Sie müssen kein vertrauenswürdiges Zertifikat verwenden. Das Zertifikat wird nur verwendet, um zu überprüfen, ob die Assembly nicht beschädigt wurde.

Führen Sie das im Microsoft Windows Software Development Kit (SDK) bereitgestellte [Pktextract.exe](pktextract-exe.md) Hilfsprogramm aus, um das öffentliche Schlüssel Token aus der Zertifikatsdatei zu extrahieren. Damit pktextract ordnungsgemäß funktioniert, muss die Zertifikat Datei im selben Verzeichnis wie das-Hilfsprogramm vorhanden sein. Verwenden Sie den extrahierten Wert des öffentlichen Schlüssel Tokens, um das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements in der Manifest-Datei zu aktualisieren.

Im folgenden finden Sie ein Beispiel für eine Manifest-Datei mit dem Namen mysampleassembly. manifest. Die Assembly mysampleassembly enthält nur eine Datei, MYFILE.DLL. Beachten Sie, dass der Wert für das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements mit dem Wert des öffentlichen Schlüssel Tokens aktualisiert wurde.

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

Führen Sie als nächstes das in der Windows SDK bereitgestellte [Mt.exe](mt-exe.md) Hilfsprogramm aus. Die Assemblydateien müssen sich im gleichen Verzeichnis befinden wie das Manifest. In diesem Beispiel ist dies das Verzeichnis mysampleassembly. Nennen Sie Mt.exe für das Beispiel wie folgt:

**c: \\ mysampleassembly>mt.exe-Manifest mysampleassembly. Manifest-hashupdate-makecdfs**

Im folgenden wird gezeigt, wie das Beispiel Manifest nach dem Ausführen Mt.exe aussieht. Beachten Sie, dass durch das Ausführen von Mt.exe mit der Option hashupdate der SHA-1-Hash der Datei hinzugefügt wird. Ändern Sie diesen Wert nicht.

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

Wenn Sie Mt.exe mit der Option-makecdfs ausführen, wird eine Datei mit dem Namen mysampleassembly. manifest. CDF generiert, in der die Inhalte des Sicherheits Katalogs beschrieben werden, der zum Validieren des Manifests verwendet wird.

Der nächste Schritt besteht darin, Makecat.exe über dieser. CDF auszuführen, um den Sicherheits Katalog für die Assembly zu erstellen. Der Makecat.exe für dieses Beispiel würde wie folgt aussehen:

**c: \\ mysampleassembly>MakeCat mysampleassembly. manifest. CDF**

Der letzte Schritt besteht darin, SignTool.exe auszuführen, um die Katalog Datei mit dem Zertifikat zu signieren. Dabei sollte es sich um das Zertifikat handeln, das in der vorhergehenden verwendet wurde, um das Token des öffentlichen Schlüssels zu generieren. Weitere Informationen zu SignTool.exe finden Sie im Thema [**SignTool**](../seccrypto/signtool.md) . Der " **SignTool** "-Befehl für das Beispiel sieht wie folgt aus:

**c: \\ mysampleassembly>SignTool Sign/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.Digicert.com MySampleAssembly.cat**

Wenn Sie über ein authentifiziertes digitales Zertifikat verfügen und Ihre Zertifizierungsstelle das PVK-Dateiformat verwendet, um den privaten Schlüssel zu speichern, können Sie den PVK Digital Certificate files-Import Programm (pvkimprt.exe) verwenden, um den Schlüssel in ihren Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu importieren. Mit diesem Hilfsprogramm können Sie in das Industriestandard Format von PFX/P12 exportieren. Weitere Informationen zum Import Programm für digitale PVK-Zertifikate finden Sie im Abschnitt Bereitstellungs Ressourcen der MSDN Library, oder wenden Sie sich an Ihre Zertifizierungsstelle. Möglicherweise können Sie pvkimprt.exe von abrufen https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Weitere Informationen finden Sie [unter Erstellen signierter Dateien und Kataloge](creating-signed-files-and-catalogs.md).

 

 
