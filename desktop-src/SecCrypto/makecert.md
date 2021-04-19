---
description: Erstellt ein X. 509-Zertifikat, das mit dem Test Stamm Schlüssel oder einem anderen angegebenen Schlüssel signiert ist, das Ihren Namen an den öffentlichen Teil des Schlüssel Paars bindet. Das Zertifikat wird in einer Datei, einem Systemzertifikat Speicher oder beiden gespeichert.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356508"
---
# <a name="makecert"></a><span data-ttu-id="84b47-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="84b47-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="84b47-105">MakeCert ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="84b47-105">MakeCert is deprecated.</span></span> <span data-ttu-id="84b47-106">Verwenden Sie zum Erstellen selbst signierter Zertifikate das PowerShell-Cmdlet [New-selfsignedcertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="84b47-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="84b47-107">Das MakeCert-Tool erstellt ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat, das mit dem Test Stamm Schlüssel oder einem anderen angegebenen Schlüssel signiert ist, das den Namen an den öffentlichen Teil des Schlüssel Paars bindet.</span><span class="sxs-lookup"><span data-stu-id="84b47-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="84b47-108">Das Zertifikat wird in einer Datei, einem Systemzertifikat Speicher oder beiden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="84b47-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="84b47-109">Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="84b47-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="84b47-110">Das MakeCert-Tool verwendet die folgende Befehlssyntax:</span><span class="sxs-lookup"><span data-stu-id="84b47-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="84b47-111">**Makecert** \[ *Basicoptions* \| *Extendedoptions* \] *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="84b47-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="84b47-112">*OutputFile* ist der Name der Datei, in die das Zertifikat geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="84b47-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="84b47-113">Sie können *OutputFile* weglassen, wenn das Zertifikat nicht in eine Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="84b47-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="84b47-114">Optionen</span><span class="sxs-lookup"><span data-stu-id="84b47-114">Options</span></span>

<span data-ttu-id="84b47-115">Makecert enthält grundlegende und erweiterte Optionen.</span><span class="sxs-lookup"><span data-stu-id="84b47-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="84b47-116">Meistens werden die Basisoptionen zum Erstellen von Zertifikaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="84b47-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="84b47-117">Die erweiterten Optionen stellen eine höhere Flexibilität zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="84b47-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="84b47-118">Die Optionen für Makecert sind auch in drei Funktionsgruppen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="84b47-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="84b47-119">Grundlegende Optionen, die nur für die Zertifikat Speichertechnologie spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="84b47-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="84b47-120">Erweiterte Optionen, die nur für die SPC-Datei und die private Schlüsseltechnologie spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="84b47-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="84b47-121">Erweiterte Optionen für die Technologie "SPC-Datei", "privater Schlüssel" und "Zertifikat Speicher".</span><span class="sxs-lookup"><span data-stu-id="84b47-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="84b47-122">Die in den folgenden Tabellen angegebenen Optionen können nur mit Internet Explorer 4,0 oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84b47-123">Basic-Option</span><span class="sxs-lookup"><span data-stu-id="84b47-123">Basic option</span></span></th>
<th><span data-ttu-id="84b47-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84b47-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84b47-125"><strong>-a</strong> <strong></strong> <em>Algorithmus</em></span><span class="sxs-lookup"><span data-stu-id="84b47-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="84b47-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="84b47-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="84b47-127">Muss entweder auf <strong>SHA-1</strong> oder <strong>MD5</strong> (Standard) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="84b47-128">Weitere Informationen zu MD5 finden Sie unter <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="84b47-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="84b47-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="84b47-130">Datum, an dem das Zertifikat zuerst gültig wird.</span><span class="sxs-lookup"><span data-stu-id="84b47-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="84b47-131">Der Standardwert ist, wenn das Zertifikat erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="84b47-131">The default is when the certificate is created.</span></span> <span data-ttu-id="84b47-132"><em>DateStart</em> hat das Format mm/dd/yyyy.</span><span class="sxs-lookup"><span data-stu-id="84b47-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-133"><strong>-CY</strong> <strong></strong> <em>Certifipeetypes</em></span><span class="sxs-lookup"><span data-stu-id="84b47-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="84b47-134">Der Zertifikattyp.</span><span class="sxs-lookup"><span data-stu-id="84b47-134">Certificate type.</span></span> <span data-ttu-id="84b47-135"><em>Certifipeetypes</em> <strong>können für die</strong> Endentität oder die Zertifizierungsstelle für die <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungs</em></a>Stelle <strong>enden</strong> .</span><span class="sxs-lookup"><span data-stu-id="84b47-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="84b47-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="84b47-137">Datum, an dem die Gültigkeitsdauer endet.</span><span class="sxs-lookup"><span data-stu-id="84b47-137">Date when the validity period ends.</span></span> <span data-ttu-id="84b47-138">Der Standardwert ist das Jahr 2039.</span><span class="sxs-lookup"><span data-stu-id="84b47-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="84b47-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="84b47-140">Fügt eine Liste mit einem oder mehreren durch Trennzeichen getrennten, <a href="/windows/desktop/SecGloss/e-gly"><em>erweiterten Schlüssel Verwendungs</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>Objekt</em></a> -IDs (OIDs) in das Zertifikat ein.</span><span class="sxs-lookup"><span data-stu-id="84b47-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="84b47-141">Beispielsweise fügt <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> die Clientauthentifizierungs-OID ein.</span><span class="sxs-lookup"><span data-stu-id="84b47-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="84b47-142">Definitionen zulässiger OIDs finden Sie in der Datei Wincrypt. h in CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="84b47-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="84b47-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="84b47-144">Maximale Höhe des Baums unter diesem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="84b47-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="84b47-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="84b47-146">Link zu den Richtlinien Informationen der SPC-Agentur (z. b. eine URL).</span><span class="sxs-lookup"><span data-stu-id="84b47-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-147"><strong>-m</strong> <strong></strong> <em>nmonate</em></span><span class="sxs-lookup"><span data-stu-id="84b47-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="84b47-148">Dauer der Gültigkeitsdauer.</span><span class="sxs-lookup"><span data-stu-id="84b47-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-149"><strong>-n</strong> <strong>&quot;</strong> <em>Name</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="84b47-150">Der Name für das Zertifikat des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="84b47-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="84b47-151">Dieser Name muss dem <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> -Standard entsprechen.</span><span class="sxs-lookup"><span data-stu-id="84b47-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="84b47-152">Die einfachste Methode besteht darin, das &quot; Format "CN =<em>myname</em> " zu verwenden &quot; .</span><span class="sxs-lookup"><span data-stu-id="84b47-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="84b47-153">Beispiel: <strong>-n &quot; CN = Test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="84b47-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="84b47-155">Die Netscape-Client Authentifizierungs Erweiterung sollte eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="84b47-157">Markiert den privaten Schlüssel als exportierbar.</span><span class="sxs-lookup"><span data-stu-id="84b47-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="84b47-159">Erstellen eines selbstsignierten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="84b47-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-160"><strong>-SC</strong> <strong></strong> " <em>Subjetcertfile</em> "</span><span class="sxs-lookup"><span data-stu-id="84b47-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="84b47-161">Der Name der Zertifikatsdatei, für die der vorhandene öffentliche Schlüssel des Antragstellers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84b47-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-162"><strong>-SK</strong> <strong></strong> <em>Subjetkey</em></span><span class="sxs-lookup"><span data-stu-id="84b47-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="84b47-163">Speicherort des Schlüssel Containers des Subjekts, der den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a>enthält.</span><span class="sxs-lookup"><span data-stu-id="84b47-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="84b47-164">Wenn kein Schlüsselcontainer vorhanden ist, wird ein Schlüsselcontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="84b47-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="84b47-165">Wenn weder die Option " <strong>-SK</strong> " noch die Option " <strong>-SV</strong> " verwendet wird, wird standardmäßig ein Standardschlüssel Container erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="84b47-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-166"><strong>-Sky</strong> <strong></strong> <em>Subjetkeyspec</em></span><span class="sxs-lookup"><span data-stu-id="84b47-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="84b47-167">Schlüssel Spezifikation des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="84b47-167">Subject's key specification.</span></span> <span data-ttu-id="84b47-168">' <em>Subjetkeyspec</em> ' muss einen von drei möglichen Werten aufweisen:</span><span class="sxs-lookup"><span data-stu-id="84b47-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="84b47-169"><strong>Signatur</strong> (AT_SIGNATURE Schlüssel Spezifikation)</span><span class="sxs-lookup"><span data-stu-id="84b47-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="84b47-170"><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüssel Spezifikation)</span><span class="sxs-lookup"><span data-stu-id="84b47-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="84b47-171">Eine ganze Zahl, z. b. <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="84b47-172">Weitere Informationen finden Sie im Hinweis in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84b47-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-173"><strong>-SP</strong> <strong></strong> <em>Subjetprovidername</em></span><span class="sxs-lookup"><span data-stu-id="84b47-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="84b47-174">Kryptoapi-Anbieter für Betreff.</span><span class="sxs-lookup"><span data-stu-id="84b47-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="84b47-175">Der Standardwert ist der Anbieter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="84b47-175">The default is the user's provider.</span></span> <span data-ttu-id="84b47-176">Weitere Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="84b47-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-177"><strong>-SR</strong> <strong></strong> <em>Subjetcertstoreloation</em></span><span class="sxs-lookup"><span data-stu-id="84b47-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="84b47-178">Der Registrierungs Speicherort für den Zertifikat Speicher des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="84b47-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="84b47-179">" <em>Subjetcertstoreloation</em> " muss entweder " <strong>LocalMachine</strong> " (Registrierungsschlüssel HKEY_LOCAL_MACHINE) oder " <strong>CurrentUser</strong> " (Registrierungsschlüssel HKEY_CURRENT_USER) sein.</span><span class="sxs-lookup"><span data-stu-id="84b47-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="84b47-180"><strong>CurrentUser</strong> ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="84b47-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-181"><strong>-SS</strong> <strong></strong> <em>Subjetcertstorename</em></span><span class="sxs-lookup"><span data-stu-id="84b47-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="84b47-182">Der Name des Zertifikats Speicher des Subjekts, in dem das generierte Zertifikat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="84b47-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-183"><strong>-SV</strong> <strong></strong> " <em>Subjetkeyfile</em> "</span><span class="sxs-lookup"><span data-stu-id="84b47-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="84b47-184">Der Name der PVK-Datei des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="84b47-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="84b47-185">Wenn weder die Option " <strong>-SK</strong> " noch die Option " <strong>-SV</strong> " verwendet wird, wird standardmäßig ein Standardschlüssel Container erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="84b47-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-186"><strong>-Sy</strong> <strong></strong> <em>nsubjetprovidertype</em></span><span class="sxs-lookup"><span data-stu-id="84b47-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="84b47-187">CryptoAPI-Anbietertyp für Betreff.</span><span class="sxs-lookup"><span data-stu-id="84b47-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="84b47-188">Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="84b47-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="84b47-189">Informationen zu kryptoapi-Anbieter Typen finden Sie in der CryptoAPI 2.0-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="84b47-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="84b47-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="84b47-191">Seriennummer des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="84b47-191">Serial number of the certificate.</span></span> <span data-ttu-id="84b47-192">Der Maximalwert ist 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="84b47-192">The maximum value is 2^31.</span></span> <span data-ttu-id="84b47-193">Der Standardwert ist ein Wert, der vom Tool generiert wird, das garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="84b47-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="84b47-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="84b47-195">Der Typ der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungs</em></a>Stelle.</span><span class="sxs-lookup"><span data-stu-id="84b47-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="84b47-196"><em>CertificateAuthority</em> muss entweder <strong>kommerziell</strong> (für Zertifikate, die von kommerziellen Software Herausgebern verwendet werden) oder <strong>Einzelpersonen</strong> (für Zertifikate, die von einzelnen Software Verlegern verwendet werden) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="84b47-198">Zeigt die grundlegenden Optionen an.</span><span class="sxs-lookup"><span data-stu-id="84b47-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="84b47-200">Zeigt die erweiterten Optionen an.</span><span class="sxs-lookup"><span data-stu-id="84b47-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="84b47-201">Wenn die Option **-Sky** Key Specification in Internet Explorer Version 4,0 oder höher verwendet wird, muss die Spezifikation mit der durch die Datei des [*privaten Schlüssels*](../secgloss/p-gly.md) oder dem privaten [*Schlüssel Container*](../secgloss/k-gly.md)gekennzeichneten Schlüssel Spezifikation identisch sein.</span><span class="sxs-lookup"><span data-stu-id="84b47-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="84b47-202">Wenn die Schlüssel Spezifikations Option nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel festgestellte Schlüssel Spezifikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="84b47-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="84b47-203">Wenn im Schlüssel Container mehr als eine Schlüssel Spezifikation vorhanden ist, wird von MakeCert zuerst versucht, die Spezifikation für den \_ Signatur Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84b47-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="84b47-204">Wenn dies fehlschlägt, versucht Makecert, bei \_ keyexchange zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84b47-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="84b47-205">Da die meisten Benutzer entweder über einen at- \_ Signatur Schlüssel oder über einen Schlüssel \_ Austausch Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="84b47-206">Die folgenden Optionen gelten nur für SPC-Dateien ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) und private Schlüsseltechnologie.</span><span class="sxs-lookup"><span data-stu-id="84b47-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84b47-207">Option "SPC und privater Schlüssel"</span><span class="sxs-lookup"><span data-stu-id="84b47-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="84b47-208">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84b47-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84b47-209"><strong>-IC</strong> <strong></strong> <em>Issuercertfile</em></span><span class="sxs-lookup"><span data-stu-id="84b47-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="84b47-210">Speicherort des Zertifikats des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="84b47-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-211"><strong>-IK</strong> <strong></strong> <em>Issuerkey</em></span><span class="sxs-lookup"><span data-stu-id="84b47-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="84b47-212">Speicherort des Schlüssel Containers des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="84b47-212">Location of the issuer's key container.</span></span> <span data-ttu-id="84b47-213">Der Standardwert ist der Test Stamm Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="84b47-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-214"><strong>-IKY</strong> <strong></strong> <em>Issuerkeyspec</em></span><span class="sxs-lookup"><span data-stu-id="84b47-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="84b47-215">Schlüssel Spezifikation des Ausstellers, die einen von drei möglichen Werten aufweisen muss:</span><span class="sxs-lookup"><span data-stu-id="84b47-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="84b47-216"><strong>Signatur</strong> (AT_SIGNATURE Schlüssel Spezifikation)</span><span class="sxs-lookup"><span data-stu-id="84b47-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="84b47-217"><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüssel Spezifikation)</span><span class="sxs-lookup"><span data-stu-id="84b47-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="84b47-218">Eine ganze Zahl, z. b. <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="84b47-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="84b47-219">Weitere Informationen finden Sie im Hinweis in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84b47-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-220"><strong>-IP</strong> <strong></strong> <em>Issuerprovidername</em></span><span class="sxs-lookup"><span data-stu-id="84b47-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="84b47-221">CryptoAPI-Anbieter für Aussteller.</span><span class="sxs-lookup"><span data-stu-id="84b47-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="84b47-222">Der Standardwert ist der Anbieter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="84b47-222">The default is the user's provider.</span></span> <span data-ttu-id="84b47-223">Weitere Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="84b47-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84b47-224"><strong>-IV</strong> <strong></strong> <em>Issuerkeyfile</em></span><span class="sxs-lookup"><span data-stu-id="84b47-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="84b47-225">Die Datei mit dem privaten Schlüssel des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="84b47-225">Issuer's private key file.</span></span> <span data-ttu-id="84b47-226">Der Standardwert ist der Test Stamm.</span><span class="sxs-lookup"><span data-stu-id="84b47-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84b47-227"><strong>-iy</strong> <strong></strong> <em>nissuerprovidertype</em></span><span class="sxs-lookup"><span data-stu-id="84b47-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="84b47-228">Der CryptoAPI-Anbietertyp für den Aussteller.</span><span class="sxs-lookup"><span data-stu-id="84b47-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="84b47-229">Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="84b47-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="84b47-230">Informationen zu kryptoapi-Anbieter Typen finden Sie in der CryptoAPI 2.0-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="84b47-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="84b47-231">Wenn die Option **-IKY** Key Specification in Internet Explorer 4,0 oder höher verwendet wird, muss die Spezifikation mit der durch die Datei des [*privaten Schlüssels*](../secgloss/p-gly.md) oder dem privaten [*Schlüssel Container*](../secgloss/k-gly.md)gekennzeichneten Schlüssel Spezifikation identisch sein.</span><span class="sxs-lookup"><span data-stu-id="84b47-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="84b47-232">Wenn die Schlüssel Spezifikations Option nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel festgestellte Schlüssel Spezifikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="84b47-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="84b47-233">Wenn im Schlüssel Container mehr als eine Schlüssel Spezifikation vorhanden ist, wird von MakeCert zuerst versucht, die Spezifikation für den \_ Signatur Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84b47-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="84b47-234">Wenn dies fehlschlägt, versucht Makecert, bei \_ keyexchange zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84b47-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="84b47-235">Da die meisten Benutzer entweder über einen at- \_ Signatur Schlüssel oder über einen Schlüssel \_ Austausch Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84b47-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="84b47-236">Die folgenden Optionen gelten nur für die [*Zertifikat Speicher*](../secgloss/c-gly.md) Technologie.</span><span class="sxs-lookup"><span data-stu-id="84b47-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="84b47-237">Zertifikat Speicher Option</span><span class="sxs-lookup"><span data-stu-id="84b47-237">Certificate store option</span></span>          | <span data-ttu-id="84b47-238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84b47-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b47-239">**-IC** *issuercertfile*</span><span class="sxs-lookup"><span data-stu-id="84b47-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="84b47-240">Die Datei, die das Zertifikat des Ausstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="84b47-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="84b47-241">Makecert sucht im Zertifikat Speicher nach einem Zertifikat mit einer genauen Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="84b47-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="84b47-242">**-in** *issuernamestring*</span><span class="sxs-lookup"><span data-stu-id="84b47-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="84b47-243">Der allgemeine Name des Zertifikats des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="84b47-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="84b47-244">Makecert sucht im Zertifikat Speicher nach einem Zertifikat, dessen gemeinsamer Name *issuernamestring* enthält.</span><span class="sxs-lookup"><span data-stu-id="84b47-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="84b47-245">**-IR** *issuercertstoreloation*</span><span class="sxs-lookup"><span data-stu-id="84b47-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="84b47-246">Der Registrierungs Speicherort für den Zertifikat Speicher des Ausstellers.</span><span class="sxs-lookup"><span data-stu-id="84b47-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="84b47-247">*Issuercertstoreloation* muss entweder **LocalMachine** (Registrierungsschlüssel HKEY \_ local \_ Machine) oder **CurrentUser** (Registrierungsschlüssel HKEY \_ aktueller \_ Benutzer) sein.</span><span class="sxs-lookup"><span data-stu-id="84b47-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="84b47-248">**CurrentUser** ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="84b47-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="84b47-249">**-ist** *issuercertstorename*</span><span class="sxs-lookup"><span data-stu-id="84b47-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="84b47-250">Der Zertifikat Speicher des Ausstellers, der das Zertifikat des Ausstellers und die zugehörigen Informationen zum privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="84b47-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="84b47-251">Wenn sich mehr als ein Zertifikat im Speicher befindet, muss der Benutzer es mithilfe der Option **-IC** oder **-in** eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="84b47-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="84b47-252">Wenn das Zertifikat im Zertifikat Speicher nicht eindeutig identifiziert wird, tritt bei Makecert ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="84b47-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
