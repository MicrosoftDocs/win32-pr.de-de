---
description: Die Funktion "Expertenstatus" gibt den Prozentsatz des Abschlusses der Expertenanalyse der Erfassungs Datei an.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Funktion "expertphestatus" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128356"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="d03d6-103">Funktion "expertindikatestatus"</span><span class="sxs-lookup"><span data-stu-id="d03d6-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="d03d6-104">Die Funktion " **Expertenstatus** " gibt den Prozentsatz des Abschlusses der Analyse der Erfassungs Datei des Experten an.</span><span class="sxs-lookup"><span data-stu-id="d03d6-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d03d6-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="d03d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d03d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d03d6-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d03d6-108">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="d03d6-108">Unique expert identifier.</span></span> <span data-ttu-id="d03d6-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d03d6-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d03d6-110">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d03d6-111">Aktueller Status der Analyse.</span><span class="sxs-lookup"><span data-stu-id="d03d6-111">Current status of the analysis.</span></span> <span data-ttu-id="d03d6-112">Geben Sie einen der folgenden Werte für " [Expertenstatus" umeration](expertstatusenumeration.md) an.</span><span class="sxs-lookup"><span data-stu-id="d03d6-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="d03d6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d03d6-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="d03d6-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d03d6-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="d03d6-115"><dt>**Profil Status \_ inaktiv**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="d03d6-116">Der Experte wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="d03d6-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="d03d6-117"><dt>**Profil Status wird \_ gestartet**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="d03d6-118">Der Experte wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="d03d6-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="d03d6-119"><dt>**Profil Status wird \_ ausgeführt**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="d03d6-120">Der Experte wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d03d6-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="d03d6-121"><dt>**expertstatus- \_ Problem**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="d03d6-122">Ein im unter Status Parameter angegebenes Problem hat den Experten beendet.</span><span class="sxs-lookup"><span data-stu-id="d03d6-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="d03d6-123"><dt>**der Expertenstatus wurde \_ abgebrochen.**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="d03d6-124">Netzwerkmonitor den Experten beendet.</span><span class="sxs-lookup"><span data-stu-id="d03d6-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="d03d6-125"><dt>**Profil Status \_ abgeschlossen**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="d03d6-126">Der Experte hat die Analyse erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d03d6-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="d03d6-127">*Unter Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d03d6-128">Erweiterung oder Erläuterung der Informationen, die vom *Status* Parameter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d03d6-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d03d6-129">*szText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d03d6-130">Optionaler Text Status Indikator.</span><span class="sxs-lookup"><span data-stu-id="d03d6-130">Optional text status indicator.</span></span>

<span data-ttu-id="d03d6-131">Dieser Parameterwert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d03d6-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d03d6-132">*Prozentuabgeschlossen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d03d6-133">Der Prozentsatz der Erfassungsdaten, die der Experte verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="d03d6-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="d03d6-134">Wenn der Experte die Analyse einer Erfassungs Datei erfolgreich abgeschlossen hat, legt das System den Prozentsatz auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="d03d6-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="d03d6-135">Jede Zahl, die größer als 99 ist, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d03d6-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d03d6-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d03d6-136">Return value</span></span>

<span data-ttu-id="d03d6-137">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d03d6-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d03d6-138">Wenn die Funktion nicht erfolgreich ist, wird der Rückgabewert nmerr- \_ Experte \_ beendet. der Experte muss sofort bereinigen und zurückkehren, ohne die Erfassung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d03d6-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="d03d6-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d03d6-139">Remarks</span></span>

<span data-ttu-id="d03d6-140">Die Funktion "-Funktion" kann nur von Experten aufgerufen werden **, die die** Exportfunktion " [Run](run.md) " oder " [configure](configure.md) " implementieren.</span><span class="sxs-lookup"><span data-stu-id="d03d6-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d03d6-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d03d6-141">Requirements</span></span>



| <span data-ttu-id="d03d6-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d03d6-142">Requirement</span></span> | <span data-ttu-id="d03d6-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d03d6-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d03d6-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d03d6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d03d6-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d03d6-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d03d6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d03d6-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d03d6-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d03d6-148">Header</span><span class="sxs-lookup"><span data-stu-id="d03d6-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d03d6-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d03d6-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d03d6-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="d03d6-151"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d03d6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d03d6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d03d6-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d03d6-153"><dt>Nmapi.dll</dt></span></span> </dl> |
