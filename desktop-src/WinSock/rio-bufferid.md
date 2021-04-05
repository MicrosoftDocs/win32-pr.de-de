---
description: Gibt einen registrierten Puffer Deskriptor an, der mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (mtausockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042011"
---
# <a name="rio_bufferid"></a><span data-ttu-id="d58c2-103">Rio \_ -bufferid</span><span class="sxs-lookup"><span data-stu-id="d58c2-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="d58c2-104">Die " **Rio \_ bufferid** typedef" gibt einen registrierten Puffer Deskriptor an, der mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d58c2-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="d58c2-105">**Rio \_ -bufferid**</span><span class="sxs-lookup"><span data-stu-id="d58c2-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="d58c2-106">Ein Datentyp, der einen registrierten Puffer Deskriptor angibt, der mit Sende-und Empfangs Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d58c2-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d58c2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d58c2-107">Remarks</span></span>

<span data-ttu-id="d58c2-108">Die registrierten Winsock-e/a-Erweiterungen arbeiten hauptsächlich bei registrierten Puffern mit **Rio \_ -bufferid-** Objekten.</span><span class="sxs-lookup"><span data-stu-id="d58c2-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="d58c2-109">Eine Anwendung erhält mit der [**rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) -Funktion eine **Rio \_ -bufferid** für einen vorhandenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="d58c2-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="d58c2-110">Eine Anwendung kann mithilfe der [**rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) -Funktion eine Registrierung freigeben.</span><span class="sxs-lookup"><span data-stu-id="d58c2-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="d58c2-111">Wenn ein vorhandener Puffer mithilfe der [**rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) -Funktion als **Rio \_ -bufferid-** Objekt registriert wird, werden bestimmte interne Ressourcen aus physischem Speicher zugeordnet, und der vorhandene Anwendungs Puffer wird in den physischen Speicher gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d58c2-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="d58c2-112">Die [**rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) -Funktion wird aufgerufen, um die Registrierung des Puffers aufzuheben, diese internen Ressourcen freizugeben und zuzulassen, dass der Puffer entsperrt und aus physischem Speicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d58c2-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="d58c2-113">Die wiederholte Registrierung und Aufhebung der Registrierung von Anwendungs Puffern mithilfe der registrierten e/a-Erweiterungen von Winsock kann zu erheblichen Leistungseinbußen führen.</span><span class="sxs-lookup"><span data-stu-id="d58c2-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="d58c2-114">Die folgenden Puffer Verwaltungsansätze sollten beim Entwerfen einer Anwendung mit den Winsock-registrierten e/a-Erweiterungen berücksichtigt werden, um die wiederholte Registrierung und Registrierung von Anwendungs Puffern zu minimieren:</span><span class="sxs-lookup"><span data-stu-id="d58c2-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="d58c2-115">• Maximieren Sie die Wiederverwendung von Puffern.</span><span class="sxs-lookup"><span data-stu-id="d58c2-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="d58c2-116">• Bewahren Sie einen eingeschränkten Pool nicht verwendeter registrierter Puffer für die Verwendung durch die Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="d58c2-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="d58c2-117">• Behalten Sie einen eingeschränkten Pool registrierter Puffer bei, und führen Sie Puffer Kopien zwischen diesen registrierten Puffern und anderen nicht registrierten Puffern aus.</span><span class="sxs-lookup"><span data-stu-id="d58c2-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="d58c2-118">Die typedef " **Rio \_ bufferid** " wird in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d58c2-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="d58c2-119">Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d58c2-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d58c2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d58c2-120">Requirements</span></span>



| <span data-ttu-id="d58c2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d58c2-121">Requirement</span></span> | <span data-ttu-id="d58c2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d58c2-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d58c2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d58c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d58c2-124">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d58c2-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="d58c2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d58c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d58c2-126">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d58c2-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="d58c2-127">Header</span><span class="sxs-lookup"><span data-stu-id="d58c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d58c2-128"><dt>Mtausockdef. h (Include mtausock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d58c2-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58c2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d58c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58c2-130">**Rio \_ buf**</span><span class="sxs-lookup"><span data-stu-id="d58c2-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="d58c2-131">**Rioderegisterbuffer**</span><span class="sxs-lookup"><span data-stu-id="d58c2-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="d58c2-132">**Rioreceive**</span><span class="sxs-lookup"><span data-stu-id="d58c2-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="d58c2-133">**Rioreceiveex**</span><span class="sxs-lookup"><span data-stu-id="d58c2-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="d58c2-134">[**Rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d58c2-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d58c2-135">**Randalisend**</span><span class="sxs-lookup"><span data-stu-id="d58c2-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="d58c2-136">[**Riosendex**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d58c2-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
