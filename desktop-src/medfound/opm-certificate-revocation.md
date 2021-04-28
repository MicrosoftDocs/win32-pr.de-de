---
description: OPM-Zertifikatsperrung
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM-Zertifikatsperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092728"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="cb269-103">OPM-Zertifikatsperrung</span><span class="sxs-lookup"><span data-stu-id="cb269-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="cb269-104">Ein OPM-Zertifikat (Output Protection Manager) kann von Microsoft widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb269-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="cb269-105">Die Liste der gesperrten Zertifikate wird in einer globalen Sperrliste (GRL) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cb269-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="cb269-106">Die GRL hat das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="cb269-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb269-107">`Section`</span><span class="sxs-lookup"><span data-stu-id="cb269-107">Section</span></span></th>
<th><span data-ttu-id="cb269-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb269-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb269-109">Header</span><span class="sxs-lookup"><span data-stu-id="cb269-109">Header</span></span></td>
<td><span data-ttu-id="cb269-110">Eine <a href="grl-header.md"><strong>GRL_HEADER</strong></a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="cb269-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb269-111">Kernspeicher</span><span class="sxs-lookup"><span data-stu-id="cb269-111">Core</span></span></td>
<td><span data-ttu-id="cb269-112">Enthält die folgenden Sperrlisten:</span><span class="sxs-lookup"><span data-stu-id="cb269-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="cb269-113">Binäre Kernelsperren</span><span class="sxs-lookup"><span data-stu-id="cb269-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="cb269-114">Binäre Sperrungen im Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="cb269-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="cb269-115">Zertifikatsperren</span><span class="sxs-lookup"><span data-stu-id="cb269-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="cb269-116">Vertrauenswürdige Stämme (reserviert)</span><span class="sxs-lookup"><span data-stu-id="cb269-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="cb269-117">Die Liste der vertrauenswürdigen Stämme wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cb269-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb269-118">Erweiterbare Einträge</span><span class="sxs-lookup"><span data-stu-id="cb269-118">Extensible entries</span></span></td>
<td><span data-ttu-id="cb269-119">Enthält Informationen, die von anderen Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb269-119">Contains information used by other components.</span></span> <span data-ttu-id="cb269-120">Dieser Abschnitt ist für OPM nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="cb269-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb269-121">Erneuerungen:</span><span class="sxs-lookup"><span data-stu-id="cb269-121">Renewals:</span></span></td>
<td><span data-ttu-id="cb269-122">Enthält GUIDs, die Windows Update definieren.</span><span class="sxs-lookup"><span data-stu-id="cb269-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="cb269-123">Dieser Abschnitt enthält Bezeichner für die folgenden Listen:</span><span class="sxs-lookup"><span data-stu-id="cb269-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="cb269-124">Binäre Kernelsperren</span><span class="sxs-lookup"><span data-stu-id="cb269-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="cb269-125">Binäre Sperrungen im Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="cb269-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="cb269-126">Zertifikatsperrungen</span><span class="sxs-lookup"><span data-stu-id="cb269-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="cb269-127">Eine Anwendung kann diese Bezeichner verwenden, um eine erneuerte Version einer gesperrten Binärdatei anzufordern, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb269-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb269-128">Signatur: Abschnitt "Core"</span><span class="sxs-lookup"><span data-stu-id="cb269-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="cb269-129">Signiert die Header- und Kernabschnitte.</span><span class="sxs-lookup"><span data-stu-id="cb269-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb269-130">Signatur: Erweiterbarer Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cb269-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="cb269-131">Signiert den Header und erweiterbare Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="cb269-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb269-132">Der GRL-Header ist eine [**\_ GRL-HEADER-Struktur.**](grl-header.md)</span><span class="sxs-lookup"><span data-stu-id="cb269-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="cb269-133">Der **dwSequenceNumber-Member** der -Struktur enthält die GRL-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="cb269-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="cb269-134">Diese Zahl wird erhöht, wenn die GRL aktualisiert und eine neue Version auf dem Computer des Benutzers platziert wird.</span><span class="sxs-lookup"><span data-stu-id="cb269-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="cb269-135">Gesperrte OPM-Zertifikate sind in der Zertifikatsperrliste des Abschnitts Core aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb269-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="cb269-136">Jeder Core-Eintrag in der GRL ist ein 20-Byte-Array, das den SHA-1-Hash des öffentlichen Schlüssels des gesperrten Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="cb269-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="cb269-137">Die Abschnitte Signatur enthalten Signaturen, mit denen überprüft werden kann, ob die GRL nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="cb269-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="cb269-138">Jeder Signaturabschnitt enthält eine [**MF \_ SIGNATURE-Struktur.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="cb269-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="cb269-139">Die erste Signatur signiert den Header und den Core-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="cb269-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="cb269-140">Die zweite Signatur signiert den Header und den Extensible-Abschnitt. Diese Signatur ist für OPM nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="cb269-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="cb269-141">Überprüfen Sie die Signatur wie folgt, um sicherzustellen, dass die GRL selbst nicht manipuliert wurde:</span><span class="sxs-lookup"><span data-stu-id="cb269-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="cb269-142">Suchen Sie den Anfang der [**MF \_ SIGNATURE-Struktur.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="cb269-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="cb269-143">Die Position der **MF \_ SIGNATURE-Struktur** wird im **cbSignatureCoreOffset-Member** der [**GRL \_ HEADER-Struktur**](grl-header.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb269-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="cb269-144">Der Speicherort wird als Offset in Bytes ab dem Anfang der GRL angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb269-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="cb269-145">Analysieren Sie die [**MF \_ SIGNATURE-Struktur**](mf-signature.md) als PKCS \# 7-Signatur mit einer Zertifikatkette.</span><span class="sxs-lookup"><span data-stu-id="cb269-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="cb269-146">Überprüfen Sie die Zertifikatkette bis zu einem vertrauenswürdigen Stamm.</span><span class="sxs-lookup"><span data-stu-id="cb269-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="cb269-147">Vergewissern Sie sich, dass das Blattzertifikat über den folgenden Objektbezeichner in der EKU verfügt: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="cb269-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="cb269-148">Berechnen Sie einen Hash der Bytes, die den Header und die Kernabschnitte der GRL enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb269-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="cb269-149">Überprüfen Sie, ob der Hash der Signatur im Blattzertifikat entspricht.</span><span class="sxs-lookup"><span data-stu-id="cb269-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb269-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb269-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb269-151">Ausgabeschutz-Manager</span><span class="sxs-lookup"><span data-stu-id="cb269-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="cb269-152">**\_GRL-HEADER**</span><span class="sxs-lookup"><span data-stu-id="cb269-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="cb269-153">**\_MF-SIGNATUR**</span><span class="sxs-lookup"><span data-stu-id="cb269-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



