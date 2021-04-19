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
# <a name="assembly-signing-example"></a><span data-ttu-id="eb0f1-103">Beispiel für die Assemblysignierung</span><span class="sxs-lookup"><span data-stu-id="eb0f1-103">Assembly Signing Example</span></span>

<span data-ttu-id="eb0f1-104">Im folgenden Beispiel wird erläutert, wie eine signierte parallele Assembly generiert wird, die aus dem Assemblymanifest, dem Überprüfungs Katalog und den Assemblydateien besteht.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="eb0f1-105">Freigegebene parallele Assemblys sollten signiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="eb0f1-106">Das Betriebssystem überprüft die Assemblysignatur vor der Installation einer freigegebenen Assembly im globalen parallelen Speicher (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="eb0f1-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="eb0f1-107">Dadurch wird es schwierig, den Herausgeber der Seite-an-Seite-Assembly zu spoomachen.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="eb0f1-108">Beachten Sie, dass das Ändern der Assemblydateien oder der Inhalt des Manifests nach der Erstellung des assemblykatalogs den Katalog und die Assembly für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="eb0f1-109">Wenn Sie die Assemblydateien oder das Manifest nach dem Erstellen und Signieren des Katalogs aktualisieren müssen, müssen Sie die Assembly erneut signieren und einen neuen Katalog generieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="eb0f1-110">Beginnen Sie mit den Assemblydateien, dem Assemblymanifest und der Zertifikatsdatei, die Sie zum Signieren der Assembly verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="eb0f1-111">Die Zertifikatsdatei muss 2048 Bit oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="eb0f1-112">Sie müssen kein vertrauenswürdiges Zertifikat verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="eb0f1-113">Das Zertifikat wird nur verwendet, um zu überprüfen, ob die Assembly nicht beschädigt wurde.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="eb0f1-114">Führen Sie das im Microsoft Windows Software Development Kit (SDK) bereitgestellte [Pktextract.exe](pktextract-exe.md) Hilfsprogramm aus, um das öffentliche Schlüssel Token aus der Zertifikatsdatei zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="eb0f1-115">Damit pktextract ordnungsgemäß funktioniert, muss die Zertifikat Datei im selben Verzeichnis wie das-Hilfsprogramm vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="eb0f1-116">Verwenden Sie den extrahierten Wert des öffentlichen Schlüssel Tokens, um das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements in der Manifest-Datei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="eb0f1-117">Im folgenden finden Sie ein Beispiel für eine Manifest-Datei mit dem Namen mysampleassembly. manifest.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="eb0f1-118">Die Assembly mysampleassembly enthält nur eine Datei, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="eb0f1-119">Beachten Sie, dass der Wert für das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements mit dem Wert des öffentlichen Schlüssel Tokens aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

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

<span data-ttu-id="eb0f1-120">Führen Sie als nächstes das in der Windows SDK bereitgestellte [Mt.exe](mt-exe.md) Hilfsprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="eb0f1-121">Die Assemblydateien müssen sich im gleichen Verzeichnis befinden wie das Manifest.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="eb0f1-122">In diesem Beispiel ist dies das Verzeichnis mysampleassembly.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="eb0f1-123">Nennen Sie Mt.exe für das Beispiel wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eb0f1-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="eb0f1-124">**c: \\ mysampleassembly>mt.exe-Manifest mysampleassembly. Manifest-hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="eb0f1-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="eb0f1-125">Im folgenden wird gezeigt, wie das Beispiel Manifest nach dem Ausführen Mt.exe aussieht.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="eb0f1-126">Beachten Sie, dass durch das Ausführen von Mt.exe mit der Option hashupdate der SHA-1-Hash der Datei hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="eb0f1-127">Ändern Sie diesen Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-127">Do not change this value.</span></span>

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

<span data-ttu-id="eb0f1-128">Wenn Sie Mt.exe mit der Option-makecdfs ausführen, wird eine Datei mit dem Namen mysampleassembly. manifest. CDF generiert, in der die Inhalte des Sicherheits Katalogs beschrieben werden, der zum Validieren des Manifests verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="eb0f1-129">Der nächste Schritt besteht darin, Makecat.exe über dieser. CDF auszuführen, um den Sicherheits Katalog für die Assembly zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="eb0f1-130">Der Makecat.exe für dieses Beispiel würde wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="eb0f1-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="eb0f1-131">**c: \\ mysampleassembly>MakeCat mysampleassembly. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="eb0f1-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="eb0f1-132">Der letzte Schritt besteht darin, SignTool.exe auszuführen, um die Katalog Datei mit dem Zertifikat zu signieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="eb0f1-133">Dabei sollte es sich um das Zertifikat handeln, das in der vorhergehenden verwendet wurde, um das Token des öffentlichen Schlüssels zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="eb0f1-134">Weitere Informationen zu SignTool.exe finden Sie im Thema [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="eb0f1-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="eb0f1-135">Der " **SignTool** "-Befehl für das Beispiel sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="eb0f1-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="eb0f1-136">**c: \\ mysampleassembly>SignTool Sign/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.Digicert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="eb0f1-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="eb0f1-137">Wenn Sie über ein authentifiziertes digitales Zertifikat verfügen und Ihre Zertifizierungsstelle das PVK-Dateiformat verwendet, um den privaten Schlüssel zu speichern, können Sie den PVK Digital Certificate files-Import Programm (pvkimprt.exe) verwenden, um den Schlüssel in ihren Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu importieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="eb0f1-138">Mit diesem Hilfsprogramm können Sie in das Industriestandard Format von PFX/P12 exportieren.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="eb0f1-139">Weitere Informationen zum Import Programm für digitale PVK-Zertifikate finden Sie im Abschnitt Bereitstellungs Ressourcen der MSDN Library, oder wenden Sie sich an Ihre Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="eb0f1-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="eb0f1-140">Möglicherweise können Sie pvkimprt.exe von abrufen https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="eb0f1-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="eb0f1-141">Weitere Informationen finden Sie [unter Erstellen signierter Dateien und Kataloge](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="eb0f1-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
