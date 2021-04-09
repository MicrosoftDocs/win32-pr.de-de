---
description: Das Microsoft Windows HTTP-Dienste (WinHTTP) Certificate Configuration Tool &\# 0034; WinHttpCertCfg.exe&\# 0034; ermöglicht Administratoren das Installieren und Konfigurieren von Client Zertifikaten in einem beliebigen Zertifikat Speicher, auf den über das Internet Server Web Application Manager-Konto (IWAM) zugegriffen werden kann. Außerdem entfällt das Tool darauf, dass Sie spezielle Konten, wie z. b. das IWAM-Konto, benötigen, um bei Verwendung von Active Server Pages (ASP) Zugriff auf Zertifikate zu erhalten.
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, ein Zertifikat Konfigurations Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129252"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="bc5b3-104">WinHttpCertCfg.exe, ein Zertifikat Konfigurations Tool</span><span class="sxs-lookup"><span data-stu-id="bc5b3-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="bc5b3-105">Das [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md) -Zertifikat Konfigurationstool "WinHttpCertCfg.exe" ermöglicht es Administratoren, Client Zertifikate in einem beliebigen [*Zertifikat Speicher*](glossary.md) zu installieren und zu konfigurieren, auf den über das Internet Server Web Application Manager-Konto (IWAM) zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="bc5b3-106">Außerdem entfällt das Tool darauf, dass Sie spezielle Konten, wie z. b. das IWAM-Konto, benötigen, um bei Verwendung von Active Server Pages (ASP) Zugriff auf Zertifikate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="bc5b3-107">Mithilfe der Microsoft Management Console (MMC) können Administratoren Client Zertifikate auf einen lokalen Computer importieren.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="bc5b3-108">Beim Importieren eines Zertifikats wird jedoch nicht automatisch der Zugriff auf den privaten Schlüssel für andere Konten gewährt.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="bc5b3-109">Dieser private Schlüssel ist für die Client Zertifikat Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="bc5b3-110">Das Microsoft Windows HTTP-Dienste (WinHTTP)-Zertifikat Konfigurationstool bietet die Möglichkeit, den Zugriff auf zusätzliche Konten (z. b. das IWAM-Konto) zu gewähren, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="bc5b3-111">Verwenden des Zertifikat Konfigurationstools</span><span class="sxs-lookup"><span data-stu-id="bc5b3-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="bc5b3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc5b3-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="bc5b3-113">Verwenden des Zertifikat Konfigurationstools</span><span class="sxs-lookup"><span data-stu-id="bc5b3-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="bc5b3-114">Das WinHTTP-Zertifikat Konfigurationstool (WinHttpCertCfg.exe) steht als Download auf der [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) -Website zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="bc5b3-115">Der folgende Beispielcode zeigt die gültigen Befehlszeilenparameter, die mit diesem Tool verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="bc5b3-116">In der folgenden Tabelle sind die Parameter für das-Konfigurationstool aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc5b3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc5b3-117">Parameter</span></span></th>
<th><span data-ttu-id="bc5b3-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc5b3-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc5b3-119">-?</span><span class="sxs-lookup"><span data-stu-id="bc5b3-119">-?</span></span></td>
<td><span data-ttu-id="bc5b3-120">Zeigt Syntax Daten an.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc5b3-121">-i</span><span class="sxs-lookup"><span data-stu-id="bc5b3-121">-i</span></span></td>
<td><span data-ttu-id="bc5b3-122">Gibt an, dass das Zertifikat aus einer PFX-Datei (Personal Information Exchange) importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="bc5b3-123">Auf diesen Parameter muss der Name der Datei folgen.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="bc5b3-124">Wenn dieser Parameter angegeben wird, &quot; &quot; müssen auch-a und &quot; -c &quot; angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc5b3-125">-g</span><span class="sxs-lookup"><span data-stu-id="bc5b3-125">-g</span></span></td>
<td><span data-ttu-id="bc5b3-126">Gibt an, dass der Zugriff auf einen privaten Schlüssel gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="bc5b3-127">Wenn dieser Parameter angegeben ist, &quot; müssen-a &quot; , &quot; -c &quot; und &quot; -s &quot; ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc5b3-128">-r</span><span class="sxs-lookup"><span data-stu-id="bc5b3-128">-r</span></span></td>
<td><span data-ttu-id="bc5b3-129">Gibt an, dass der Zugriff für einen privaten Schlüssel entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="bc5b3-130">Wenn dieser Parameter angegeben ist, &quot; müssen-a &quot; , &quot; -c &quot; und &quot; -s &quot; ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc5b3-131">-l</span><span class="sxs-lookup"><span data-stu-id="bc5b3-131">-l</span></span></td>
<td><span data-ttu-id="bc5b3-132">Gibt an, dass Konten mit Zugriff auf einen privaten Schlüssel aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="bc5b3-133">Wenn dieser Parameter angegeben wird, &quot; &quot; müssen auch-c und &quot; -s &quot; angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc5b3-134">-a</span><span class="sxs-lookup"><span data-stu-id="bc5b3-134">-a</span></span></td>
<td><span data-ttu-id="bc5b3-135">Gibt das Benutzerkonto auf dem Computer an, der konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="bc5b3-136">Dabei kann es sich um ein lokales Computer-oder Domänen Konto handeln, wie z &quot; &quot; . b. IWAM_TESTMACHINE, &quot; testuser &quot; oder &quot; testdomain\domainuser &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc5b3-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc5b3-137">-c</span><span class="sxs-lookup"><span data-stu-id="bc5b3-137">-c</span></span></td>
<td><span data-ttu-id="bc5b3-138">Gibt den Speicherort und den Namen des <a href="glossary.md"><em>Zertifikat Speicher</em></a>an.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="bc5b3-139">Verwenden &quot; &quot; Sie LOCAL_MACHINE oder &quot; CURRENT_USER &quot; , um zu bestimmen, welcher registrierungsbranch für den Speicherort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="bc5b3-140">Der <em>Zertifikat Speicher</em> kann alle auf dem Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="bc5b3-141">Typische namens Beispiele sind &quot; My &quot; , &quot; root &quot; und &quot; treuhändpeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc5b3-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="bc5b3-142">Der Speicherort und der Name des <em>Zertifikat Speicher</em> sind durch einen umgekehrten Schrägstrich getrennt, z &quot; . b. LOCAL_MACHINE \Root &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc5b3-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bc5b3-143">Obwohl der &quot; CURRENT_USER &quot; Branch der Registrierung mit diesem Parameter angegeben werden kann, ist das Erweitern des Zugriffs auf private Schlüssel hauptsächlich für Zertifikate vorgesehen, die in einem <a href="glossary.md"><em>Zertifikat Speicher</em></a> des lokalen Computers installiert sind und auf den von mehreren Benutzern zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc5b3-144">-S</span><span class="sxs-lookup"><span data-stu-id="bc5b3-144">-s</span></span></td>
<td><span data-ttu-id="bc5b3-145">Gibt eine Such Zeichenfolge ohne Beachtung der Groß-/Kleinschreibung für die Suche nach dem ersten aufgelisteten Zertifikat mit einem Antragsteller Namen an</span><span class="sxs-lookup"><span data-stu-id="bc5b3-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc5b3-146">-p</span><span class="sxs-lookup"><span data-stu-id="bc5b3-146">-p</span></span></td>
<td><span data-ttu-id="bc5b3-147">Gibt ein Kennwort an, das verwendet wird, um das Zertifikat und den privaten Schlüssel zu importieren.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="bc5b3-148">Diese Option wird nur mit der Import-Option verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="bc5b3-149">Der Benutzer muss über ausreichende Berechtigungen verfügen, um dieses Tool verwenden zu können. Dies erfordert, dass der Benutzer ein Administrator und derselbe Benutzer ist, der das Client Zertifikat installiert hat, sofern es installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="bc5b3-150">Das Tool "WinHttpCertCfg.exe" ist nicht nützlich, um in einem Dateisystem wie FAT32 gespeicherte Zertifikate zu konfigurieren, die keine Zugriffs Steuerungs Listen (Access Control Lists, ACL) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="bc5b3-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc5b3-151">Examples</span></span>

<span data-ttu-id="bc5b3-152">Die folgenden Beispiele zeigen einige Möglichkeiten, wie das-Konfigurationstool verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="bc5b3-153">Mit diesem Befehl werden Konten aufgelistet, die Zugriff auf den privaten Schlüssel für das Zertifikat "myCertificate" im [*Zertifikat Speicher*](glossary.md) "root" des lokalen \_ Computer Branchs der Registrierung haben.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="bc5b3-154">**Winhttpcertcfg-l-c lokale \_ Computer Stamm \\ -s myCertificate**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="bc5b3-155">Mit diesem Befehl wird der Zugriff auf den privaten Schlüssel des Zertifikats "myCertificate" im [*Zertifikat Speicher*](glossary.md) "My" für das testuser-Konto gewährt.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="bc5b3-156">**Winhttpcertcfg-g-c lokaler \_ Computer \\ My-s myCertificate-a testuser**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="bc5b3-157">Dieser Befehl importiert ein Zertifikat und einen privaten Schlüssel aus einer PFX-Datei und erweitert den privaten Schlüssel Zugriff auf ein anderes Konto.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="bc5b3-158">**Winhttpcertcfg-i pfxfile-c lokaler \_ Computer \\ My-a IWAM \_ testmachine-p pfxpassword**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="bc5b3-159">Dieser Befehl verweigert den Zugriff auf den privaten Schlüssel für das IWAM- \_ testmachine-Konto mit dem angegebenen Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="bc5b3-160">**Winhttpcertcfg-r-c lokale \_ Computer Stamm \\ -s myCertificate-a IWAM \_ testmachine**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




