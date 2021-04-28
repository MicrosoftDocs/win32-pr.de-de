---
description: 'IESP::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: IESP::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103768"
---
# <a name="iespstop-method"></a><span data-ttu-id="bd497-103">IESP::Stop-Methode</span><span class="sxs-lookup"><span data-stu-id="bd497-103">IESP::Stop method</span></span>

<span data-ttu-id="bd497-104">Die **Stop-Methode** beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="bd497-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd497-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd497-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="bd497-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd497-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd497-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd497-108">Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die Netzwerkstatistiken enthält, z. B. gesamt erfasste Frames und gesamt erfasste Bytes.</span><span class="sxs-lookup"><span data-stu-id="bd497-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd497-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd497-109">Return value</span></span>

<span data-ttu-id="bd497-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="bd497-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bd497-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="bd497-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bd497-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bd497-112">Return code</span></span>                                                                                          | <span data-ttu-id="bd497-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd497-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd497-114"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="bd497-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bd497-115">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="bd497-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="bd497-116">Rufen Sie [IESP::Connect](iesp-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="bd497-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bd497-117"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="bd497-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="bd497-118">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="bd497-118">The NPP is not capturing data.</span></span> <span data-ttu-id="bd497-119">Rufen Sie [IESP::Start](iesp-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="bd497-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="bd497-120"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="bd497-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="bd497-121">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IESP::Connect-Methode.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="bd497-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bd497-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd497-122">Remarks</span></span>

<span data-ttu-id="bd497-123">Wenn die **IESP::Stop-Methode** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungsdatei.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="bd497-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="bd497-124">(Der Name der Erfassungsdatei wurde zurückgegeben, als [IESP::Start](iesp-start.md) aufgerufen wurde.) Sie können sich nun den Inhalt der Aufzeichnungsdatei ansehen.</span><span class="sxs-lookup"><span data-stu-id="bd497-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="bd497-125">Wenn Sie die Erfassung beenden und neu starten, müssen Sie jedes Mal die [IESP::Configure-Methode](iesp-configure.md) aufrufen, wenn Sie [IESP::Start](iesp-start.md) aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="bd497-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd497-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd497-126">Requirements</span></span>



| <span data-ttu-id="bd497-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd497-127">Requirement</span></span> | <span data-ttu-id="bd497-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bd497-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd497-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd497-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bd497-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd497-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bd497-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd497-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bd497-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd497-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bd497-133">Header</span><span class="sxs-lookup"><span data-stu-id="bd497-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd497-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd497-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bd497-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bd497-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd497-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd497-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd497-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd497-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd497-138">IESP</span><span class="sxs-lookup"><span data-stu-id="bd497-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="bd497-139">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="bd497-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="bd497-140">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="bd497-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="bd497-141">Statistiken</span><span class="sxs-lookup"><span data-stu-id="bd497-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




