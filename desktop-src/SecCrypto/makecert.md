---
description: Erstellt ein vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiertes X.509-Zertifikat, das Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet. Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c15db364066d9edadb6a0c4d2c24dceab5cc9
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327144"
---
# <a name="makecert"></a><span data-ttu-id="aff0d-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="aff0d-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="aff0d-105">MakeCert ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-105">MakeCert is deprecated.</span></span> <span data-ttu-id="aff0d-106">Verwenden Sie das PowerShell-Cmdlet [New-SelfSignedCertificate,](/powershell/module/pki/new-selfsignedcertificate)um selbstsignierte Zertifikate zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aff0d-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="aff0d-107">Das MakeCert-Tool erstellt ein [*X.509-Zertifikat,*](../secgloss/x-gly.md) das vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiert wurde, das Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="aff0d-108">Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aff0d-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="aff0d-109">Das Tool wird im \\ Ordner Bin des Installationspfads microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="aff0d-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="aff0d-110">Das MakeCert-Tool verwendet die folgende Befehlssyntax:</span><span class="sxs-lookup"><span data-stu-id="aff0d-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="aff0d-111">**MakeCert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="aff0d-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="aff0d-112">*OutputFile* ist der Name der Datei, in die das Zertifikat geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aff0d-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="aff0d-113">Sie können *OutputFile* weglassen, wenn das Zertifikat nicht in eine Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="aff0d-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="aff0d-114">Optionen</span><span class="sxs-lookup"><span data-stu-id="aff0d-114">Options</span></span>

<span data-ttu-id="aff0d-115">MakeCert enthält grundlegende und erweiterte Optionen.</span><span class="sxs-lookup"><span data-stu-id="aff0d-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="aff0d-116">Meistens werden die Basisoptionen zum Erstellen von Zertifikaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="aff0d-117">Die erweiterten Optionen stellen eine höhere Flexibilität zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aff0d-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="aff0d-118">Die Optionen für MakeCert sind auch in drei Funktionsgruppen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="aff0d-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="aff0d-119">Grundlegende Optionen, die nur für Zertifikatspeichertechnologie spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="aff0d-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="aff0d-120">Erweiterte Optionen, die nur für SPC-Datei- und Private Key-Technologie spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="aff0d-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="aff0d-121">Erweiterte Optionen für SPC-Datei, privaten Schlüssel und Zertifikatspeichertechnologie.</span><span class="sxs-lookup"><span data-stu-id="aff0d-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="aff0d-122">Die in den folgenden Tabellen angegebenen Optionen können nur mit Internet Explorer 4.0 oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0d-123">Basic-Option</span><span class="sxs-lookup"><span data-stu-id="aff0d-123">Basic option</span></span></th>
<th><span data-ttu-id="aff0d-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aff0d-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff0d-125"><strong>-a</strong> <strong></strong> <em>Algorithmus</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="aff0d-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hashalgorithmus.</em></a></span><span class="sxs-lookup"><span data-stu-id="aff0d-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="aff0d-127">Muss entweder auf <strong>SHA-1</strong> oder <strong>MD5</strong> (Standard) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="aff0d-128">Informationen zu MD5 finden Sie unter <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="aff0d-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="aff0d-130">Datum, an dem das Zertifikat zuerst gültig wird.</span><span class="sxs-lookup"><span data-stu-id="aff0d-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="aff0d-131">Der Standardwert ist, wenn das Zertifikat erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="aff0d-131">The default is when the certificate is created.</span></span> <span data-ttu-id="aff0d-132">Das Format von <em>DateStart</em> ist mm/tt/yyyy.</span><span class="sxs-lookup"><span data-stu-id="aff0d-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="aff0d-134">Zertifikattyp.</span><span class="sxs-lookup"><span data-stu-id="aff0d-134">Certificate type.</span></span> <span data-ttu-id="aff0d-135"><em>CertificateTypes können</em> end <strong>für end-entity</strong> oder <strong>authority for</strong> certification <a href="/windows/desktop/SecGloss/c-gly"><em>authority sein.</em></a></span><span class="sxs-lookup"><span data-stu-id="aff0d-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="aff0d-137">Datum, an dem die Gültigkeitsdauer endet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-137">Date when the validity period ends.</span></span> <span data-ttu-id="aff0d-138">Der Standardwert ist das Jahr 2039.</span><span class="sxs-lookup"><span data-stu-id="aff0d-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-139"><strong>-eku</strong> <strong></strong> <em>OID1,</em><strong></strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="aff0d-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="aff0d-140">Fügt eine Liste von durch Komma <a href="/windows/desktop/SecGloss/e-gly"><em>getrennten,</em></a> erweiterten Schlüsselverwendungsobjektbezeichnern (OIDs) in das Zertifikat ein. <a href="/windows/desktop/SecGloss/o-gly"><em></em></a></span><span class="sxs-lookup"><span data-stu-id="aff0d-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="aff0d-141">Beispielsweise fügt <strong>-eku 1.3.6.1.5.5.7.3.2</strong> die Clientauthentifizierungs-OID ein.</span><span class="sxs-lookup"><span data-stu-id="aff0d-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="aff0d-142">Definitionen von zulässigen OIDs finden Sie in der Datei Wincrypt.h in CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="aff0d-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="aff0d-144">Maximale Höhe der Struktur unter diesem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="aff0d-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="aff0d-146">Link zu Richtlinieninformationen der SPC-Agentur (z. B. eine URL).</span><span class="sxs-lookup"><span data-stu-id="aff0d-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="aff0d-148">Dauer der Gültigkeitsdauer.</span><span class="sxs-lookup"><span data-stu-id="aff0d-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-149"><strong>-n</strong> <strong>&quot;</strong> <em>Name</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="aff0d-150">Name für das Zertifikat des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="aff0d-151">Dieser Name muss dem <a href="/windows/desktop/SecGloss/x-gly"><em>X.500-Standard</em></a> entsprechen.</span><span class="sxs-lookup"><span data-stu-id="aff0d-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="aff0d-152">Die einfachste Methode ist die Verwendung des &quot; CN=<em>MyName-Formats.</em> &quot;</span><span class="sxs-lookup"><span data-stu-id="aff0d-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="aff0d-153">Beispiel: <strong>-n &quot; CN=Test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="aff0d-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="aff0d-155">Die Netscape-Clientauthentifizierungserweiterung sollte enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="aff0d-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-156"><strong>-pe</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="aff0d-157">Markiert den privaten Schlüssel als exportierbar.</span><span class="sxs-lookup"><span data-stu-id="aff0d-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="aff0d-159">Erstellen eines selbstsignierten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="aff0d-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="aff0d-161">Name der Zertifikatdatei mit dem vorhandenen öffentlichen Schlüssel des Antragstellers, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aff0d-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="aff0d-163">Speicherort des Schlüsselcontainers des Antragstellers, der den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a>enthält.</span><span class="sxs-lookup"><span data-stu-id="aff0d-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="aff0d-164">Wenn kein Schlüsselcontainer vorhanden ist, wird ein Schlüsselcontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="aff0d-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="aff0d-165">Wenn weder die Option <strong>-sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="aff0d-167">Schlüsselspezifikation des Antragstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-167">Subject's key specification.</span></span> <span data-ttu-id="aff0d-168"><em>SubjectKeySpec</em> muss einer von drei möglichen Werten sein:</span><span class="sxs-lookup"><span data-stu-id="aff0d-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="aff0d-169"><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</span><span class="sxs-lookup"><span data-stu-id="aff0d-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="aff0d-170"><strong>Exchange</strong> (AT_KEYEXCHANGE Schlüsselspezifikation)</span><span class="sxs-lookup"><span data-stu-id="aff0d-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="aff0d-171">Eine ganze Zahl, z. <strong>B. 3</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="aff0d-172">Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.</span><span class="sxs-lookup"><span data-stu-id="aff0d-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="aff0d-174">CryptoAPI-Anbieter für Betreff.</span><span class="sxs-lookup"><span data-stu-id="aff0d-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="aff0d-175">Der Standardwert ist der Anbieter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-175">The default is the user's provider.</span></span> <span data-ttu-id="aff0d-176">Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0 Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff0d-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="aff0d-178">Der Registrierungsspeicherort des Zertifikatspeichers des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="aff0d-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="aff0d-179"><em>SubjectCertStoreLocation</em> muss entweder <strong>LocalMachine (Registrierungsschlüssel</strong> HKEY_LOCAL_MACHINE) oder <strong>CurrentUser</strong> (Registrierungsschlüssel)HKEY_CURRENT_USER.</span><span class="sxs-lookup"><span data-stu-id="aff0d-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="aff0d-180"><strong>CurrentUser</strong> ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="aff0d-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="aff0d-182">Name des Zertifikatspeichers des Subjekts, in dem das generierte Zertifikat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="aff0d-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="aff0d-184">Name der PVK-Datei des Betreffs.</span><span class="sxs-lookup"><span data-stu-id="aff0d-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="aff0d-185">Wenn weder <strong>die Option -sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="aff0d-187">CryptoAPI-Anbietertyp für Betreff.</span><span class="sxs-lookup"><span data-stu-id="aff0d-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="aff0d-188">Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="aff0d-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="aff0d-189">Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0 Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff0d-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="aff0d-191">Seriennummer des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="aff0d-191">Serial number of the certificate.</span></span> <span data-ttu-id="aff0d-192">Der Höchstwert ist 2^31.</span><span class="sxs-lookup"><span data-stu-id="aff0d-192">The maximum value is 2^31.</span></span> <span data-ttu-id="aff0d-193">Der Standardwert ist ein vom Tool generierter Wert, der garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="aff0d-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="aff0d-195">Typ der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungsstelle.</em></a></span><span class="sxs-lookup"><span data-stu-id="aff0d-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="aff0d-196"><em>CertificateAuthority</em> muss entweder auf <strong>"commercial"</strong> (für Zertifikate, die von kommerziellen Softwareverlegern verwendet werden sollen) oder <strong>"Individual"</strong> (für Zertifikate, die von einzelnen Softwareverlegern verwendet werden sollen) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="aff0d-198">Zeigt die grundlegenden Optionen an.</span><span class="sxs-lookup"><span data-stu-id="aff0d-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="aff0d-200">Zeigt die erweiterten Optionen an.</span><span class="sxs-lookup"><span data-stu-id="aff0d-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="aff0d-201">Wenn die -sky-Schlüsselspezifikationsoption in Internet Explorer Version 4.0 oder höher verwendet wird, muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) oder den [*Privaten Schlüsselcontainer*](../secgloss/k-gly.md)angegeben wird. </span><span class="sxs-lookup"><span data-stu-id="aff0d-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="aff0d-202">Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die durch die Datei mit dem privaten Schlüssel oder den Privaten Schlüsselcontainer angegebene Schlüsselspezifikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="aff0d-203">Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen vorhanden sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="aff0d-204">Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="aff0d-205">Da die meisten Benutzer entweder über einen AT \_ SIGNATURE-Schlüssel oder einen AT \_ KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="aff0d-206">Die folgenden Optionen gelten nur für SPC-Dateien [*(Software Publisher Certificate)*](../secgloss/s-gly.md) und Technologie für private Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="aff0d-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0d-207">SPC- und private Schlüsseloption</span><span class="sxs-lookup"><span data-stu-id="aff0d-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="aff0d-208">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aff0d-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff0d-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="aff0d-210">Speicherort des Zertifikats des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="aff0d-212">Speicherort des Schlüsselcontainers des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-212">Location of the issuer's key container.</span></span> <span data-ttu-id="aff0d-213">Der Standardwert ist der Teststammschlüssel.</span><span class="sxs-lookup"><span data-stu-id="aff0d-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="aff0d-215">Die Schlüsselspezifikation des Ausstellers, die einer von drei möglichen Werten sein muss:</span><span class="sxs-lookup"><span data-stu-id="aff0d-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="aff0d-216"><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</span><span class="sxs-lookup"><span data-stu-id="aff0d-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="aff0d-217"><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüsselspezifikation)</span><span class="sxs-lookup"><span data-stu-id="aff0d-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="aff0d-218">Eine ganze Zahl, z. <strong>B. 3</strong></span><span class="sxs-lookup"><span data-stu-id="aff0d-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="aff0d-219">Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.</span><span class="sxs-lookup"><span data-stu-id="aff0d-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="aff0d-221">CryptoAPI-Anbieter für Aussteller.</span><span class="sxs-lookup"><span data-stu-id="aff0d-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="aff0d-222">Der Standardwert ist der Anbieter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-222">The default is the user's provider.</span></span> <span data-ttu-id="aff0d-223">Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0 Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff0d-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0d-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="aff0d-225">Die Datei mit dem privaten Schlüssel des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-225">Issuer's private key file.</span></span> <span data-ttu-id="aff0d-226">Der Standardwert ist der Teststamm.</span><span class="sxs-lookup"><span data-stu-id="aff0d-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0d-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="aff0d-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="aff0d-228">CryptoAPI-Anbietertyp für Aussteller.</span><span class="sxs-lookup"><span data-stu-id="aff0d-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="aff0d-229">Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="aff0d-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="aff0d-230">Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0 Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff0d-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="aff0d-231">Wenn die **Option -iky** key specification in Internet Explorer 4.0 oder höher verwendet wird, [](../secgloss/p-gly.md) muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei mit dem privaten Schlüssel oder den Privaten Schlüsselcontainer [*angegeben wird.*](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="aff0d-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="aff0d-232">Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel angegebene Schlüsselspezifikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff0d-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="aff0d-233">Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen enthalten sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="aff0d-234">Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="aff0d-235">Da die meisten Benutzer entweder über einen AT \_ SIGNATURE-Schlüssel oder einen AT \_ KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff0d-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="aff0d-236">Die folgenden Optionen gelten nur für [*Zertifikatspeichertechnologien.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="aff0d-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="aff0d-237">Zertifikatspeicheroption</span><span class="sxs-lookup"><span data-stu-id="aff0d-237">Certificate store option</span></span>          | <span data-ttu-id="aff0d-238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aff0d-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff0d-239">**-ic** *IssuerCertFile*</span><span class="sxs-lookup"><span data-stu-id="aff0d-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="aff0d-240">Datei, die das Zertifikat des Ausstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="aff0d-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="aff0d-241">MakeCert sucht im Zertifikatspeicher nach einem Zertifikat mit einer genauen Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="aff0d-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="aff0d-242">**-in** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="aff0d-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="aff0d-243">Allgemeiner Name des Zertifikats des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="aff0d-244">MakeCert sucht im Zertifikatspeicher nach einem Zertifikat, dessen allgemeiner Name *IssuerNameString* enthält.</span><span class="sxs-lookup"><span data-stu-id="aff0d-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="aff0d-245">**-ir** *IssuerCertStoreLocation*</span><span class="sxs-lookup"><span data-stu-id="aff0d-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="aff0d-246">Registrierungsspeicherort des Zertifikatspeichers des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="aff0d-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="aff0d-247">*IssuerCertStoreLocation* muss entweder **LocalMachine** (Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE) oder **CurrentUser** (Registrierungsschlüssel HKEY \_ CURRENT \_ USER) sein.</span><span class="sxs-lookup"><span data-stu-id="aff0d-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="aff0d-248">**CurrentUser** ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="aff0d-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="aff0d-249">**-is** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="aff0d-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="aff0d-250">Der Zertifikatspeicher des Ausstellers, der das Zertifikat des Ausstellers und die zugehörigen Informationen zum privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="aff0d-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="aff0d-251">Wenn mehr als ein Zertifikat im Speicher vorhanden ist, muss der Benutzer es mithilfe der Option **-ic** oder **-in** eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aff0d-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="aff0d-252">Wenn das Zertifikat im Zertifikatspeicher nicht eindeutig identifiziert wird, schlägt MakeCert fehl.</span><span class="sxs-lookup"><span data-stu-id="aff0d-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
