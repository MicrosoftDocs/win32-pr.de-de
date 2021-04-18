---
title: Ideliveryoptimizationjob ADDFILEWITHRANGES-Methode (deliveryoptimization. h)
description: Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- ADDFILEWITHRANGES-Methode
- ADDFILEWITHRANGES-Methode, ideliveryoptimizationjob-Schnittstelle
- Ideliveryoptimizationjob-Schnittstelle, ADDFILEWITHRANGES-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341037"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="9b40f-106">Ideliveryoptimizationjob:: ADDFILEWITHRANGES-Methode</span><span class="sxs-lookup"><span data-stu-id="9b40f-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="9b40f-107">Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b40f-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b40f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b40f-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="9b40f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b40f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b40f-110">nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-111">Eine NULL beendete Zeichenfolge, die ein eindeutiger Bezeichner für den veröffentlichten Inhalt ist.</span><span class="sxs-lookup"><span data-stu-id="9b40f-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="9b40f-112">Bei nicht veröffentlichten Inhalten kann dies eine beliebige eindeutige Zeichenfolge sein, mit der der Aufrufer Dateien innerhalb eines Auftrags identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="9b40f-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="9b40f-113">*RemoteURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-114">Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Server enthält.</span><span class="sxs-lookup"><span data-stu-id="9b40f-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="9b40f-115">*localname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-116">Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Client enthält.</span><span class="sxs-lookup"><span data-stu-id="9b40f-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="9b40f-117">*rangecount* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-118">Anzahl der Elemente in *Bereichen*.</span><span class="sxs-lookup"><span data-stu-id="9b40f-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="9b40f-119">*Bereiche* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-120">Array aus mindestens einer [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) -Struktur, die die Bereiche angeben, die heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b40f-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="9b40f-121">Geben Sie keine doppelten oder überlappenden Bereiche an.</span><span class="sxs-lookup"><span data-stu-id="9b40f-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="9b40f-122">*FileSize* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b40f-123">Die Länge der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9b40f-123">Size of the file in bytes.</span></span> <span data-ttu-id="9b40f-124">Übergeben Sie **DO_UNKNOWN_FILE_SIZE** , wenn die Größe der aufruferanwendung nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9b40f-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b40f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b40f-125">Return value</span></span>

<span data-ttu-id="9b40f-126">Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="9b40f-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b40f-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9b40f-127">Return code</span></span></th>
<th><span data-ttu-id="9b40f-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b40f-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9b40f-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-130">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9b40f-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9b40f-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-132">Der lokale Dateiname ist NULL oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b40f-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9b40f-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-134">Der Benutzer verfügt nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="9b40f-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9b40f-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-136">Einer der Bereiche ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9b40f-136">One of the ranges is invalid.</span></span> <span data-ttu-id="9b40f-137">Beispielsweise ist initialoffset auf <strong>BG_LENGTH_TO_EOF</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b40f-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9b40f-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-139">Doppelte oder überlappende Bereiche können nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b40f-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b40f-140">Die Bereiche werden nach dem Offset des Werts sortiert, nicht nach der Länge.</span><span class="sxs-lookup"><span data-stu-id="9b40f-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="9b40f-141">Wenn Bereiche eingegeben werden, die den gleichen Offset aufweisen, aber in umgekehrter Reihenfolge sind, wird dieser Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b40f-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="9b40f-142">Wenn z. b. 100,5 und 100,0 in dieser Reihenfolge eingegeben werden, können Sie die Datei nicht dem Auftrag hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9b40f-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9b40f-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b40f-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9b40f-144">Der Status des Auftrags kann nicht <strong>BG_JOB_STATE_CANCELLED</strong> oder <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="9b40f-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9b40f-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b40f-145">Requirements</span></span>



| <span data-ttu-id="9b40f-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b40f-146">Requirement</span></span> | <span data-ttu-id="9b40f-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9b40f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b40f-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b40f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9b40f-149">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9b40f-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b40f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9b40f-151">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b40f-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9b40f-152">Header</span><span class="sxs-lookup"><span data-stu-id="9b40f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b40f-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b40f-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b40f-154">IDL</span><span class="sxs-lookup"><span data-stu-id="9b40f-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b40f-155"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b40f-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b40f-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b40f-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b40f-157"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b40f-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9b40f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9b40f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b40f-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b40f-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9b40f-160">IID</span><span class="sxs-lookup"><span data-stu-id="9b40f-160">IID</span></span><br/>                      | <span data-ttu-id="9b40f-161">IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert.</span><span class="sxs-lookup"><span data-stu-id="9b40f-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9b40f-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b40f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b40f-163">**Ideliveryoptimizationjob**</span><span class="sxs-lookup"><span data-stu-id="9b40f-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 

