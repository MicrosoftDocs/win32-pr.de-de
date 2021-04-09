---
title: App-Objekt-Manager (MakeAppx.exe)
description: App Packager (MakeAppx.exe) erstellt ein App-Paket aus Dateien auf dem Datenträger oder extrahiert die Dateien aus einem App-Paket auf einen Datenträger.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101467"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="78c74-103">App-Objekt-Manager (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="78c74-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="78c74-104">Eine UWP-Anleitung zur Verwendung dieses Tools finden Sie unter [Erstellen eines App-Pakets mit dem MakeAppx.exe Tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="78c74-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="78c74-105">App Packager (MakeAppx.exe) erstellt ein App-Paket aus Dateien auf dem Datenträger oder extrahiert die Dateien aus einem App-Paket auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="78c74-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="78c74-106">Ab Windows 8.1 erstellt App Packager auch ein App-Paket Paket aus app-Paketen auf einem Datenträger oder extrahiert die APP-Pakete aus einem App-Paket auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="78c74-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="78c74-107">Es ist in Microsoft Visual Studio und im Windows Software Development Kit (SDK) für Windows 8 oder Windows Software Development Kit (SDK) für Windows 8.1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="78c74-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="78c74-108">Besuchen Sie [Downloads für Entwickler]( https://msdn.microsoft.com/windows/apps/br229516.aspx) , um diese zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="78c74-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="78c74-109">Das MakeAppx.exe Tool befindet sich in der Regel an den folgenden Orten:</span><span class="sxs-lookup"><span data-stu-id="78c74-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="78c74-110">Auf x86: C: \\ Program Files (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="78c74-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="78c74-111">Auf x64 an zwei Orten:</span><span class="sxs-lookup"><span data-stu-id="78c74-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="78c74-112">C: \\ Programme (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="78c74-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="78c74-113">C: \\ Programme (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="78c74-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="78c74-114">Es gibt keine Arm-Version des Tools.</span><span class="sxs-lookup"><span data-stu-id="78c74-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="78c74-115">So erstellen Sie ein Paket mit einer Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="78c74-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="78c74-116">So erstellen Sie ein Paket mit einer Mapping-Datei</span><span class="sxs-lookup"><span data-stu-id="78c74-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="78c74-117">So signieren Sie das Paket mit SignTool</span><span class="sxs-lookup"><span data-stu-id="78c74-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="78c74-118">So extrahieren Sie Dateien aus einem Paket</span><span class="sxs-lookup"><span data-stu-id="78c74-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="78c74-119">So erstellen Sie ein Paket Bündel mithilfe einer Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="78c74-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="78c74-120">So erstellen Sie ein Paket Bündel mithilfe einer Mapping-Datei</span><span class="sxs-lookup"><span data-stu-id="78c74-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="78c74-121">So extrahieren Sie Pakete aus einem Bündel</span><span class="sxs-lookup"><span data-stu-id="78c74-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="78c74-122">So verschlüsseln Sie ein Paket mit einer Schlüsseldatei</span><span class="sxs-lookup"><span data-stu-id="78c74-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="78c74-123">So verschlüsseln Sie ein Paket mit einem globalen Testschlüssel</span><span class="sxs-lookup"><span data-stu-id="78c74-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="78c74-124">So entschlüsseln Sie ein Paket mit einer Schlüsseldatei</span><span class="sxs-lookup"><span data-stu-id="78c74-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="78c74-125">So entschlüsseln Sie ein Paket mit einem globalen Testschlüssel</span><span class="sxs-lookup"><span data-stu-id="78c74-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="78c74-126">Verwendung</span><span class="sxs-lookup"><span data-stu-id="78c74-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="78c74-127">Verwenden von App Packager</span><span class="sxs-lookup"><span data-stu-id="78c74-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="78c74-128">Relative Pfade werden im gesamten Tool unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78c74-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="78c74-129">So erstellen Sie ein Paket mit einer Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="78c74-129">To create a package using a directory structure</span></span>

<span data-ttu-id="78c74-130">Platzieren Sie die AppxManifest.xml im Stammverzeichnis eines Verzeichnisses, das alle Nutz Last Dateien für Ihre APP enthält.</span><span class="sxs-lookup"><span data-stu-id="78c74-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="78c74-131">Eine identische Verzeichnisstruktur wird für das App-Paket erstellt und ist verfügbar, wenn das Paket zum Zeitpunkt der Bereitstellung extrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="78c74-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="78c74-132">Platzieren Sie alle Dateien in einer einzelnen Verzeichnisstruktur, und erstellen Sie nach Wunsch Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="78c74-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="78c74-133">Erstellen Sie ein gültiges Paket Manifest, AppxManifest.xml, und platzieren Sie es im Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="78c74-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="78c74-134">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-134">Run this command:</span></span>

    <span data-ttu-id="78c74-135">**Makeappx Pack/d** *input \_ directerypath* **/p** _FilePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="78c74-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="78c74-136">So erstellen Sie ein Paket mit einer Mapping-Datei</span><span class="sxs-lookup"><span data-stu-id="78c74-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="78c74-137">Erstellen Sie ein gültiges Paket Manifest, AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="78c74-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="78c74-138">Erstellen Sie eine Mapping-Datei.</span><span class="sxs-lookup"><span data-stu-id="78c74-138">Create a mapping file.</span></span> <span data-ttu-id="78c74-139">Die erste Zeile enthält die Zeichen folgen **\[ Dateien \]**, und in den nachfolgenden Zeilen werden die Quell-(Datenträger) und Ziel Pfade (Paket) in Zeichen folgen in Anführungszeichen angegeben.</span><span class="sxs-lookup"><span data-stu-id="78c74-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="78c74-140">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-140">Run this command:</span></span>

    <span data-ttu-id="78c74-141">**Makeappx Pack/f** *Mapping \_ FilePath* **/p** _FilePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="78c74-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="78c74-142">So signieren Sie das Paket mit SignTool</span><span class="sxs-lookup"><span data-stu-id="78c74-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="78c74-143">Erstellen Sie das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="78c74-143">Create the certificate.</span></span> <span data-ttu-id="78c74-144">Der im Manifest aufgelistete Verleger muss mit den Informationen des Verleger Antragstellers des Signatur Zertifikats identisch sein.</span><span class="sxs-lookup"><span data-stu-id="78c74-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="78c74-145">Weitere Informationen zum Erstellen eines Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="78c74-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="78c74-146">Führen Sie SignTool.exe aus, um das Paket zu signieren:</span><span class="sxs-lookup"><span data-stu-id="78c74-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="78c74-147">**SignTool Sign/a/v/FD** *HashAlgorithm* **/f** *certfilename* _FilePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="78c74-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="78c74-148">*HashAlgorithm* muss mit dem Hash Algorithmus, der zum Erstellen der blockmap verwendet wurde, beim Verpacken der App entsprechen.</span><span class="sxs-lookup"><span data-stu-id="78c74-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="78c74-149">Mit dem Hilfsprogramm makeappx-Paket ist der standardmäßige AppX blockmap-Hash Algorithmus **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="78c74-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="78c74-150">Führen Sie SignTool.exe mit Angabe von **SHA256** als File Digest-Algorithmus (/FD) aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="78c74-151">**SignTool Sign/a/v/FD SHA256/f** *certfilename* _FilePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="78c74-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="78c74-152">Weitere Informationen zum Signieren von Paketen finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="78c74-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="78c74-153">So extrahieren Sie Dateien aus einem Paket</span><span class="sxs-lookup"><span data-stu-id="78c74-153">To extract files from a package</span></span>

1.  <span data-ttu-id="78c74-154">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-154">Run this command:</span></span>

    <span data-ttu-id="78c74-155">**Makeappx entpacken/p** _File_**. AppX/d** *Ausgabe \_ Verzeichnis*</span><span class="sxs-lookup"><span data-stu-id="78c74-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="78c74-156">Das entpackte Paket hat die gleiche Struktur wie das installierte Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="78c74-157">So erstellen Sie ein Paket Bündel mithilfe einer Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="78c74-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="78c74-158">Wir verwenden den **Bundle** -Befehl, um eine APP Bundle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c74-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="78c74-159">durch das Hinzufügen aller Pakete aus <content directory> (einschließlich Unterordnern).</span><span class="sxs-lookup"><span data-stu-id="78c74-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="78c74-160">Wenn <content directory> ein Bündel Manifest enthält, wird AppxBundleManifest.xml ignoriert.</span><span class="sxs-lookup"><span data-stu-id="78c74-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="78c74-161">Platzieren Sie alle Pakete in einer einzelnen Verzeichnisstruktur, und erstellen Sie nach Wunsch Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="78c74-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="78c74-162">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-162">Run this command:</span></span>

    <span data-ttu-id="78c74-163">**Makeappx Bundle/d** *input \_ directoriypath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="78c74-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="78c74-164">So erstellen Sie ein Paket Bündel mithilfe einer Mapping-Datei</span><span class="sxs-lookup"><span data-stu-id="78c74-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="78c74-165">Wir verwenden den **Bundle** -Befehl, um eine APP Bundle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c74-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="78c74-166">durch das Hinzufügen aller Pakete aus einer Liste von Paketen in <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="78c74-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="78c74-167">Wenn <mapping file> ein Bündel Manifest enthält, wird AppxBundleManifest.xml ignoriert.</span><span class="sxs-lookup"><span data-stu-id="78c74-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="78c74-168">Erstellen Sie eine <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="78c74-168">Create a <mapping file>.</span></span> <span data-ttu-id="78c74-169">Die erste Zeile enthält die Zeichen folgen **\[ Dateien \]**, und in den folgenden Zeilen werden die Pakete angegeben, die dem Paket hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="78c74-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="78c74-170">Jedes Paket wird durch ein paar von Pfaden in Anführungszeichen, getrennt durch Leerzeichen oder Registerkarten, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78c74-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="78c74-171">Das Pfad paar stellt die Quelle des Pakets (auf dem Datenträger) und das Ziel (in Bundle) dar.</span><span class="sxs-lookup"><span data-stu-id="78c74-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="78c74-172">Alle Ziel Paketnamen müssen die Erweiterung ". AppX" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="78c74-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="78c74-173">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-173">Run this command:</span></span>

    <span data-ttu-id="78c74-174">**Makeappx Bundle/f** *Mapping \_ FilePath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="78c74-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="78c74-175">So extrahieren Sie Pakete aus einem Bündel</span><span class="sxs-lookup"><span data-stu-id="78c74-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="78c74-176">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-176">Run this command:</span></span>

    <span data-ttu-id="78c74-177">**Makeappx entflechten/p** _Bundle \_ Name_**. appxbundle/d** *Ausgabe \_ Verzeichnis*</span><span class="sxs-lookup"><span data-stu-id="78c74-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="78c74-178">Das entpackte Paket hat die gleiche Struktur wie das installierte Paket Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="78c74-179">So verschlüsseln Sie ein Paket mit einer Schlüsseldatei</span><span class="sxs-lookup"><span data-stu-id="78c74-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="78c74-180">Erstellen Sie eine Schlüsseldatei.</span><span class="sxs-lookup"><span data-stu-id="78c74-180">Create a key file.</span></span> <span data-ttu-id="78c74-181">Schlüsseldateien müssen mit einer Zeile beginnen, die die Zeichenfolge " \[ Keys \] " enthält, gefolgt von Zeilen, in denen die Schlüssel zum Verschlüsseln des Pakets beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="78c74-182">Jeder Schlüssel wird durch ein paar von Zeichen folgen in Anführungszeichen, getrennt durch Leerzeichen oder Tabstopps, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78c74-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="78c74-183">Die erste Zeichenfolge stellt die Schlüssel-ID dar, und die zweite Zeichenfolge stellt den Verschlüsselungsschlüssel in hexadezimaler Form dar.</span><span class="sxs-lookup"><span data-stu-id="78c74-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="78c74-184">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-184">Run this command:</span></span>

    <span data-ttu-id="78c74-185">**MakeAppx.exe verschlüsseln/p** _\_ Paketname_**. AppX/EP** _verschlüsselter \_ \_ Paketname_.**eappx/KF** _KeyFile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="78c74-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="78c74-186">Das Eingabe Paket wird mithilfe der angegebenen Schlüsseldatei in das angegebene verschlüsselte Paket verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="78c74-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="78c74-187">So verschlüsseln Sie ein Paket mit einem globalen Testschlüssel</span><span class="sxs-lookup"><span data-stu-id="78c74-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="78c74-188">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-188">Run this command:</span></span>

    <span data-ttu-id="78c74-189">**MakeAppx.exe verschlüsseln/p** _\_ Paketname_**. AppX/EP** _verschlüsselter \_ \_ Paketname_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="78c74-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="78c74-190">Das Eingabe Paket wird mithilfe des globalen Test Schlüssels in das angegebene verschlüsselte Paket verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="78c74-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="78c74-191">So entschlüsseln Sie ein Paket mit einer Schlüsseldatei</span><span class="sxs-lookup"><span data-stu-id="78c74-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="78c74-192">Erstellen Sie eine Schlüsseldatei.</span><span class="sxs-lookup"><span data-stu-id="78c74-192">Create a key file.</span></span> <span data-ttu-id="78c74-193">Schlüsseldateien müssen mit einer Zeile beginnen, die die Zeichenfolge " \[ Keys \] " enthält, gefolgt von Zeilen, in denen die Schlüssel zum Verschlüsseln des Pakets beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="78c74-194">Jeder Schlüssel wird durch ein paar von Zeichen folgen in Anführungszeichen, getrennt durch Leerzeichen oder Tabstopps, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78c74-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="78c74-195">Die erste Zeichenfolge stellt die Base64-codierte 32-Byte-Schlüssel-ID und die zweite Zeichenfolge den Base64-codierten 32-Byte-Verschlüsselungsschlüssel dar.</span><span class="sxs-lookup"><span data-stu-id="78c74-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="78c74-196">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-196">Run this command:</span></span>

    <span data-ttu-id="78c74-197">**MakeAppx.exe entschlüsseln/p** _\_ Paketname_**. AppX/EP** _unverschlüsselter \_ \_ Paketname_**. eappx/KF** _KeyFile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="78c74-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="78c74-198">Das Eingabe Paket wird mithilfe der angegebenen Schlüsseldatei in das angegebene unverschlüsselte Paket entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="78c74-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="78c74-199">So entschlüsseln Sie ein Paket mit einem globalen Testschlüssel</span><span class="sxs-lookup"><span data-stu-id="78c74-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="78c74-200">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="78c74-200">Run this command:</span></span>

    <span data-ttu-id="78c74-201">**MakeAppx.exe entschlüsseln/p** _\_ Paketname_**. AppX/EP** _unverschlüsselter \_ \_ Paketname_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="78c74-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="78c74-202">Das Eingabe Paket wird mithilfe des globalen Test Schlüssels in das angegebene unverschlüsselte Paket entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="78c74-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="78c74-203">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="78c74-203">Usage</span></span>

<span data-ttu-id="78c74-204">Das Befehlszeilenargument **/p** ist immer erforderlich, entweder mit **/d**, **/f** oder **/EP**.</span><span class="sxs-lookup"><span data-stu-id="78c74-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="78c74-205">Beachten Sie, dass sich **/d**, **/f** und **/EP** gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="78c74-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="78c74-206">**Makeappx Pack \[ - \] Optionen** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="78c74-207">**Makeappx Pack \[ - \] Optionen** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="78c74-208">**Makeappx entpacken \[ - \] Optionen** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="78c74-209">**Makeappx- \[ Bündel \] Optionen** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="78c74-210">**Makeappx- \[ Bündel \] Optionen** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="78c74-211">**Makeappx entflechten \[ - \] Optionen** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="78c74-212">**Makeappx- \[ Verschlüsselungs \] Optionen** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="78c74-213">**Makeappx- \[ \] Entschlüsselungen** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="78c74-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="78c74-214">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="78c74-214">Command-line Syntax</span></span>

<span data-ttu-id="78c74-215">Hier ist die allgemeine Syntax Syntax für die Befehlszeile für makeappx.</span><span class="sxs-lookup"><span data-stu-id="78c74-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="78c74-216">**Makeappx \[ Pack \| Entpacken \| des Pakets \| \| \| \] entflechten verschlüsseln** \[ **/h** **/KF** **/KT** **/l** **/o** **/No** **/NV** **/v** **/PFN** **/?**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="78c74-217">**Makeappx** verpackt bzw. entpackt die Dateien in einem Paket, bündelt oder entpackt die Pakete in einem Paket oder verschlüsselt oder entschlüsselt das App-Paket oder Paket im angegebenen Eingabe Verzeichnis bzw. in der Zuordnungsdatei.</span><span class="sxs-lookup"><span data-stu-id="78c74-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="78c74-218">Im folgenden finden Sie eine Liste der Parameter, die für **makeappx Pack**, **makeappx entpacken**, **makeappx Bundle**, **makeappx entflechten**, **makeappx verschlüsseln** oder **makeappx entschlüsseln** gelten.</span><span class="sxs-lookup"><span data-stu-id="78c74-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="78c74-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-220">Diese Option wird für lokalisierte Pakete verwendet.</span><span class="sxs-lookup"><span data-stu-id="78c74-220">This option is used for localized packages.</span></span> <span data-ttu-id="78c74-221">Die Standardüberprüfung wird durch lokalisierte Pakete ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="78c74-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="78c74-222">Mit dieser Option wird nur diese spezifische Validierung deaktiviert, ohne dass die gesamte Validierung deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="78c74-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="78c74-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-224">Überschreiben Sie die Ausgabedatei, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="78c74-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="78c74-225">Wenn Sie diese Option oder die Option **/No** nicht angeben, wird der Benutzer gefragt, ob die Datei überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c74-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="78c74-226">Sie können diese Option nicht mit **/No** verwenden.</span><span class="sxs-lookup"><span data-stu-id="78c74-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-227"><span id="_no"></span><span id="_NO"></span>**/no**</span><span class="sxs-lookup"><span data-stu-id="78c74-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-228">Verhindert ein Überschreiben der Ausgabedatei, wenn vorhanden.</span><span class="sxs-lookup"><span data-stu-id="78c74-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="78c74-229">Wenn Sie diese Option oder die Option **/o** nicht angeben, wird der Benutzer gefragt, ob die Datei überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c74-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="78c74-230">Sie können diese Option nicht mit **/o** verwenden.</span><span class="sxs-lookup"><span data-stu-id="78c74-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="78c74-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-232">Überspringen der semantischen Validierung.</span><span class="sxs-lookup"><span data-stu-id="78c74-232">Skip semantic validation.</span></span> <span data-ttu-id="78c74-233">Wenn Sie diese Option nicht angeben, führt das Tool eine vollständige Überprüfung des Pakets aus.</span><span class="sxs-lookup"><span data-stu-id="78c74-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="78c74-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-235">Aktivieren Sie die ausführliche Protokollierungs Ausgabe in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="78c74-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="78c74-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-237">Hilfetext anzeigen.</span><span class="sxs-lookup"><span data-stu-id="78c74-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="78c74-238">**Makeappx Pack** , **makeappx entpacken** , **makeappx Bundle**, **makeappx entflechten**, **makeappx verschlüsseln** und **makeappx entschlüsseln** sind sich gegenseitig ausschließende Befehle.</span><span class="sxs-lookup"><span data-stu-id="78c74-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="78c74-239">Hier sind die Befehlszeilenparameter aufgeführt, die speziell für jeden Befehl gelten:</span><span class="sxs-lookup"><span data-stu-id="78c74-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="78c74-240">**Makeappx-Paket** \[ **h**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="78c74-241">Erstellt ein Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** - *Algorithmus*</span><span class="sxs-lookup"><span data-stu-id="78c74-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="78c74-243">Gibt den Hashalgorithmus an, der beim Erstellen der Blockzuordnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78c74-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="78c74-244">Im folgenden finden Sie gültige Werte für den- *Algorithmus*:</span><span class="sxs-lookup"><span data-stu-id="78c74-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="78c74-245">SHA256 (Standard)</span><span class="sxs-lookup"><span data-stu-id="78c74-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="78c74-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="78c74-246">SHA384</span></span></dd> <dd><span data-ttu-id="78c74-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="78c74-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="78c74-248">Diese Option kann nicht mit dem **Entpacken** -Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="78c74-249">**Makeappx entpacken** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="78c74-250">Extrahiert alle Dateien im angegebenen Paket in das angegebene Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="78c74-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="78c74-251">Die Ausgabe hat dieselbe Verzeichnisstruktur wie das Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="78c74-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-253">Gibt ein Verzeichnis namens mit dem vollständigen Paketnamen an.</span><span class="sxs-lookup"><span data-stu-id="78c74-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="78c74-254">Dieses Verzeichnis wird unter dem angegebenen Ausgabe Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="78c74-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="78c74-255">Diese Option kann nicht mit dem Befehl **Pack** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="78c74-256">**Makeappx-Paket** \[ Entpacken **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="78c74-257">Entpackt alle Pakete in ein Unterverzeichnis unter dem angegebenen Ausgabepfad, benannt nach dem vollständigen Paketnamen.</span><span class="sxs-lookup"><span data-stu-id="78c74-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="78c74-258">Die Ausgabe hat dieselbe Verzeichnisstruktur wie das Paket mit installiertem Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="78c74-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-260">Gibt ein Verzeichnis mit dem Namen des Paket Bündel vollständig an.</span><span class="sxs-lookup"><span data-stu-id="78c74-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="78c74-261">Dieses Verzeichnis wird unter dem angegebenen Ausgabe Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="78c74-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="78c74-262">Diese Option kann nicht mit dem **Bundle** -Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="78c74-263">**Makeappx verschlüsseln** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="78c74-264">Erstellt im angegebenen Ausgabe Paket ein verschlüsseltes App-Paket aus dem angegebenen Eingabe-App-Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="78c74-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="78c74-266">Verschlüsselt das Paket oder Paket mithilfe des Schlüssels aus der angegebenen Schlüsseldatei.</span><span class="sxs-lookup"><span data-stu-id="78c74-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="78c74-267">Diese Option kann nicht mit **KT** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="78c74-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-269">Verschlüsselt das Paket oder Paket mit dem globalen Testschlüssel.</span><span class="sxs-lookup"><span data-stu-id="78c74-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="78c74-270">Diese Option kann nicht mit **KF** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="78c74-271">**Makeappx-Entschlüsselung** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="78c74-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="78c74-272">Erstellt ein unverschlüsseltes App-Paket aus dem angegebenen Eingabe-App-Paket im angegebenen Ausgabe Paket.</span><span class="sxs-lookup"><span data-stu-id="78c74-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="78c74-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="78c74-274">Entschlüsselt das Paket oder Paket mithilfe des Schlüssels aus der angegebenen Schlüsseldatei.</span><span class="sxs-lookup"><span data-stu-id="78c74-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="78c74-275">Diese Option kann nicht mit **KT** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="78c74-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="78c74-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="78c74-277">Entschlüsselt das Paket oder Paket mit dem globalen Testschlüssel.</span><span class="sxs-lookup"><span data-stu-id="78c74-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="78c74-278">Diese Option kann nicht mit **KF** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c74-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="78c74-279">Durch makeappx ausgeführte Semantik Validierung</span><span class="sxs-lookup"><span data-stu-id="78c74-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="78c74-280">Makeappx führt eine eingeschränkte Semantik Überprüfung durch, mit der die häufigsten Bereitstellungs Fehler abgefangen und sichergestellt werden, dass das App-Paket gültig ist.</span><span class="sxs-lookup"><span data-stu-id="78c74-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="78c74-281">Diese Überprüfung stellt Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="78c74-281">This validation ensures that:</span></span>

-   <span data-ttu-id="78c74-282">Alle Dateien, auf die im Paketmanifest verwiesen wird, sind im App-Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="78c74-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="78c74-283">Die Anwendung besitzt nicht zwei identische Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="78c74-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="78c74-284">Eine Anwendung registriert sich nicht für ein unzulässiges Protokoll aus dieser Liste: SMB, File, MS-WWA-Web, MS-WWA.</span><span class="sxs-lookup"><span data-stu-id="78c74-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="78c74-285">Diese semantische Validierung ist nicht fertiggestellt, und die von makeappx erstellten Pakete sind nicht garantiert installier Bar.</span><span class="sxs-lookup"><span data-stu-id="78c74-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 