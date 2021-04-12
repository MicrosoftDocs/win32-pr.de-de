---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM-Zertifikat Sperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527890"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="345ba-103">OPM-Zertifikat Sperrung</span><span class="sxs-lookup"><span data-stu-id="345ba-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="345ba-104">Ein Ausgabe Schutz-Manager-Zertifikat (OPM) kann von Microsoft gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="345ba-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="345ba-105">Die Liste der gesperrten Zertifikate wird in einer globalen Sperr Liste (GRL) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="345ba-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="345ba-106">Die GRL weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="345ba-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="345ba-107">`Section`</span><span class="sxs-lookup"><span data-stu-id="345ba-107">Section</span></span></th>
<th><span data-ttu-id="345ba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="345ba-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="345ba-109">Header</span><span class="sxs-lookup"><span data-stu-id="345ba-109">Header</span></span></td>
<td><span data-ttu-id="345ba-110">Eine <a href="grl-header.md"><strong>GRL_HEADER</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="345ba-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="345ba-111">Kernspeicher</span><span class="sxs-lookup"><span data-stu-id="345ba-111">Core</span></span></td>
<td><span data-ttu-id="345ba-112">Enthält die folgenden Sperr Listen:</span><span class="sxs-lookup"><span data-stu-id="345ba-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="345ba-113">Binäre Kernel-Sperren</span><span class="sxs-lookup"><span data-stu-id="345ba-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="345ba-114">Binäre widerrufen im Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="345ba-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="345ba-115">Zertifikat Widerruf</span><span class="sxs-lookup"><span data-stu-id="345ba-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="345ba-116">Vertrauenswürdige Stämme (reserviert)</span><span class="sxs-lookup"><span data-stu-id="345ba-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="345ba-117">Die Liste der vertrauenswürdigen Stämme wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="345ba-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="345ba-118">Erweiterbare Einträge</span><span class="sxs-lookup"><span data-stu-id="345ba-118">Extensible entries</span></span></td>
<td><span data-ttu-id="345ba-119">Enthält Informationen, die von anderen Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="345ba-119">Contains information used by other components.</span></span> <span data-ttu-id="345ba-120">Dieser Abschnitt ist für OPM nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="345ba-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="345ba-121">Erneuerungen</span><span class="sxs-lookup"><span data-stu-id="345ba-121">Renewals:</span></span></td>
<td><span data-ttu-id="345ba-122">Enthält GUIDs, die Windows Update Bezeichner definieren.</span><span class="sxs-lookup"><span data-stu-id="345ba-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="345ba-123">Dieser Abschnitt enthält Bezeichner für die folgenden Listen:</span><span class="sxs-lookup"><span data-stu-id="345ba-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="345ba-124">Binäre Kernel-Sperren</span><span class="sxs-lookup"><span data-stu-id="345ba-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="345ba-125">Binäre widerrufen im Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="345ba-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="345ba-126">Zertifikat Widerruf</span><span class="sxs-lookup"><span data-stu-id="345ba-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="345ba-127">Eine Anwendung kann diese Bezeichner verwenden, um eine erneuerte Version einer gesperrten Binärdatei anzufordern, sofern eine solche vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="345ba-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="345ba-128">Signatur: Abschnitt "Core"</span><span class="sxs-lookup"><span data-stu-id="345ba-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="345ba-129">Signiert die Header-und Kern Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="345ba-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="345ba-130">Signatur: erweiterbarer Abschnitt</span><span class="sxs-lookup"><span data-stu-id="345ba-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="345ba-131">Signiert den Header und erweiterbare Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="345ba-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="345ba-132">Der GRL-Header ist eine [**GRL- \_ Header**](grl-header.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="345ba-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="345ba-133">Der **dwsequencenenumber** -Member der-Struktur enthält die GRL-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="345ba-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="345ba-134">Diese Zahl wird bei jedem Update der GRL und einer neuen Version auf dem Computer des Benutzers inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="345ba-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="345ba-135">Widerrufene OPM-Zertifikate werden in der Liste der Zertifikat Widerrufungen des Core-Abschnitts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="345ba-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="345ba-136">Jeder Kern Eintrag in der GRL ist ein 20-Byte-Array, das den SHA-1-Hash des öffentlichen Schlüssels des widerrufenen Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="345ba-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="345ba-137">Die Signatur Abschnitte enthalten Signaturen, die verwendet werden können, um zu überprüfen, ob die GRL nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="345ba-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="345ba-138">Jeder Signatur Abschnitt enthält die "am MF"- [**\_ Signatur**](mf-signature.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="345ba-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="345ba-139">Die erste Signatur signiert den Header und den Abschnitt Core.</span><span class="sxs-lookup"><span data-stu-id="345ba-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="345ba-140">Die zweite Signatur signiert den Header und den erweiterbaren Abschnitt. Diese Signatur ist für OPM nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="345ba-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="345ba-141">Um sicherzustellen, dass die GRL selbst nicht manipuliert wurde, überprüfen Sie die Signatur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="345ba-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="345ba-142">Ermitteln des Starts der [**MF- \_ Signatur**](mf-signature.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="345ba-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="345ba-143">Der Speicherort der **MF- \_ Signatur** Struktur wird im **cbsignaturecoreoffset** -Member der [**GRL- \_ Header**](grl-header.md) Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="345ba-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="345ba-144">Der Speicherort wird als Offset in Bytes vom Anfang der GRL angegeben.</span><span class="sxs-lookup"><span data-stu-id="345ba-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="345ba-145">Analysieren Sie die [**MF- \_ Signatur**](mf-signature.md) Struktur als PKCS \# 7-Signatur mit einer Zertifikat Kette.</span><span class="sxs-lookup"><span data-stu-id="345ba-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="345ba-146">Überprüfen Sie die Zertifikat Kette bis zu einer vertrauenswürdigen Stamm Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="345ba-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="345ba-147">Vergewissern Sie sich, dass das Blatt Zertifikat den folgenden Objekt Bezeichner in der EKU enthält: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="345ba-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="345ba-148">Berechnen Sie einen Hashwert der Bytes, die den Header und die Kern Abschnitte der GRL enthalten.</span><span class="sxs-lookup"><span data-stu-id="345ba-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="345ba-149">Vergewissern Sie sich, dass der Hash mit der Signatur im Blatt Zertifikat übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="345ba-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="345ba-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="345ba-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="345ba-151">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="345ba-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="345ba-152">**GRL- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="345ba-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="345ba-153">**MF- \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="345ba-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



