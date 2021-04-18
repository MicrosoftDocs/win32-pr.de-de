---
description: Stellt Funktionen zum Signieren von ausführbaren Dateien mit einer digitalen Authenticode-Signatur bereit.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Signedcode-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365658"
---
# <a name="signedcode-object"></a><span data-ttu-id="33b38-103">Signedcode-Objekt</span><span class="sxs-lookup"><span data-stu-id="33b38-103">SignedCode object</span></span>

<span data-ttu-id="33b38-104">\[Das **signedcode** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="33b38-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="33b38-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="33b38-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="33b38-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="33b38-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="33b38-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="33b38-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="33b38-108">Das **signedcode** -Objekt stellt Funktionen zum Signieren von ausführbaren Dateien mit einer digitalen Authenticode-Signatur bereit.</span><span class="sxs-lookup"><span data-stu-id="33b38-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="33b38-109">Verwendung</span><span class="sxs-lookup"><span data-stu-id="33b38-109">When to use</span></span>

<span data-ttu-id="33b38-110">Das **signedcode** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="33b38-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="33b38-111">Signieren Sie ausführbare Dateien.</span><span class="sxs-lookup"><span data-stu-id="33b38-111">Sign executable files.</span></span>
-   <span data-ttu-id="33b38-112">Ausführbare Dateien für Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="33b38-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="33b38-113">Bestimmen Sie, ob die Signatur der ausführbaren Datei gültig ist.</span><span class="sxs-lookup"><span data-stu-id="33b38-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="33b38-114">Legen Sie den Pfad zur ausführbaren Datei fest oder rufen Sie ihn ab.</span><span class="sxs-lookup"><span data-stu-id="33b38-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="33b38-115">Rufen Sie den Signatur Geber und den Zeitstempel der ausführbaren Datei ab.</span><span class="sxs-lookup"><span data-stu-id="33b38-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="33b38-116">Ruft eine Sammlung der Zertifikate für die ausführbare Datei ab.</span><span class="sxs-lookup"><span data-stu-id="33b38-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="33b38-117">Rufen Sie eine Beschreibung oder die URL zur Beschreibung der ausführbaren Datei ab.</span><span class="sxs-lookup"><span data-stu-id="33b38-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="33b38-118">Member</span><span class="sxs-lookup"><span data-stu-id="33b38-118">Members</span></span>

<span data-ttu-id="33b38-119">Das **signedcode** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="33b38-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="33b38-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="33b38-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="33b38-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33b38-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33b38-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="33b38-122">Methods</span></span>

<span data-ttu-id="33b38-123">Das **signedcode** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="33b38-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="33b38-124">Methode</span><span class="sxs-lookup"><span data-stu-id="33b38-124">Method</span></span>                                    | <span data-ttu-id="33b38-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33b38-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33b38-126">**Gebärden**</span><span class="sxs-lookup"><span data-stu-id="33b38-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="33b38-127">Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="33b38-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="33b38-128">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="33b38-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="33b38-129">Erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="33b38-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="33b38-130">**Weisen**</span><span class="sxs-lookup"><span data-stu-id="33b38-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="33b38-131">Überprüft die Authenticode-Signatur in der signierten ausführbaren Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="33b38-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="33b38-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33b38-132">Properties</span></span>

<span data-ttu-id="33b38-133">Das **signedcode** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="33b38-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="33b38-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33b38-134">Property</span></span>                                                       | <span data-ttu-id="33b38-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="33b38-135">Access type</span></span>           | <span data-ttu-id="33b38-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33b38-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33b38-137">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="33b38-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="33b38-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33b38-138">Read-only</span></span><br/>  | <span data-ttu-id="33b38-139">Eine [**Zertifikat**](certificates.md) Sammlung, die alle Zertifikate in der signierten ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="33b38-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="33b38-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33b38-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="33b38-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33b38-141">Read/write</span></span><br/> | <span data-ttu-id="33b38-142">Eine Zeichenfolge, die eine Beschreibung der signierten ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="33b38-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="33b38-143">**Deskriptionurl**</span><span class="sxs-lookup"><span data-stu-id="33b38-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="33b38-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33b38-144">Read/write</span></span><br/> | <span data-ttu-id="33b38-145">Eine Zeichenfolge, die die http-Adresse für eine Beschreibung der signierten ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="33b38-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="33b38-146">**FileName**</span><span class="sxs-lookup"><span data-stu-id="33b38-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="33b38-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33b38-147">Read/write</span></span><br/> | <span data-ttu-id="33b38-148">Eine Zeichenfolge, die den Pfad zur Inhalts Datei enthält, die die ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="33b38-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="33b38-149">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="33b38-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="33b38-150">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="33b38-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="33b38-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33b38-151">Read-only</span></span><br/>  | <span data-ttu-id="33b38-152">Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Signatur Geber der ausführbaren Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="33b38-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="33b38-153">**Timestamper**</span><span class="sxs-lookup"><span data-stu-id="33b38-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="33b38-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33b38-154">Read-only</span></span><br/>  | <span data-ttu-id="33b38-155">Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Zeitstempel der ausführbaren Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="33b38-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="33b38-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33b38-156">Remarks</span></span>

<span data-ttu-id="33b38-157">Das **signedcode** -Objekt kann erstellt werden und ist für die Skripterstellung nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="33b38-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="33b38-158">Die ProgID für das **signedcode** -Objekt ist CAPICOM. Signedcode. 1.</span><span class="sxs-lookup"><span data-stu-id="33b38-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="33b38-159">Die ausführbare Datei muss einen Typ aufweisen, der mit Authenticode-Technologie signiert werden kann, z. b. Dateien mit der Dateinamenerweiterung ". cab", ". cat", ". exe", ". dll", ". vb" oder ". ocx".</span><span class="sxs-lookup"><span data-stu-id="33b38-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b38-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b38-160">Requirements</span></span>



| <span data-ttu-id="33b38-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b38-161">Requirement</span></span> | <span data-ttu-id="33b38-162">Wert</span><span class="sxs-lookup"><span data-stu-id="33b38-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b38-163">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="33b38-163">Redistributable</span></span><br/> | <span data-ttu-id="33b38-164">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="33b38-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="33b38-165">DLL</span><span class="sxs-lookup"><span data-stu-id="33b38-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="33b38-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b38-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
