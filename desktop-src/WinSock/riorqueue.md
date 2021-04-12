---
description: Gibt einen socketdeskriptor an, der von Sende-und Empfangs Anforderungen mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (mtausockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344739"
---
# <a name="rio_rq"></a><span data-ttu-id="435bc-103">Rio \_ RQ</span><span class="sxs-lookup"><span data-stu-id="435bc-103">RIO\_RQ</span></span>

<span data-ttu-id="435bc-104">Die **Rio \_ RQ** -typedef gibt einen socketdeskriptor an, der von Sende-und Empfangs Anforderungen mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="435bc-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="435bc-105">**Rio \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="435bc-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="435bc-106">Ein Datentyp, der einen von Sende-und Empfangs Anforderungen verwendeten socketdeskriptor angibt.</span><span class="sxs-lookup"><span data-stu-id="435bc-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="435bc-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="435bc-107">Remarks</span></span>

<span data-ttu-id="435bc-108">Die registrierten Winsock-e/a-Erweiterungen arbeiten hauptsächlich auf einem **Rio- \_ RQ** -Objekt und nicht auf einem Socket.</span><span class="sxs-lookup"><span data-stu-id="435bc-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="435bc-109">Eine Anwendung erhält einen **Rio \_ RQ** für einen vorhandenen Socket mithilfe der " [**riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) "-Funktion.</span><span class="sxs-lookup"><span data-stu-id="435bc-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="435bc-110">Der Eingabe Socket muss durch Aufrufen der [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion erstellt worden sein, wobei das **WSA- \_ Flag " \_ Rio** " im Parameter " *dwFlags* " festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="435bc-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="435bc-111">Nachdem Sie ein **Rio- \_ RQ** -Objekt abgerufen haben, bleibt der zugrunde liegende socketdeskriptor gültig.</span><span class="sxs-lookup"><span data-stu-id="435bc-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="435bc-112">Eine Anwendung kann den zugrunde liegenden Socket weiterhin verwenden, um Socketoptionen festzulegen und abzufragen, IOCTLs auszugeben und schließlich den Socket zu schließen.</span><span class="sxs-lookup"><span data-stu-id="435bc-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="435bc-113">Der Zugriff auf die Vervollständigungs Warteschlangen ([**Rio- \_ CQ**](riocqueue.md) -Strukturen) und Anforderungs Warteschlangen (**Rio \_ RQ** -Strukturen) werden aus Gründen der Effizienz nicht durch Synchronisierungs primitive geschützt.</span><span class="sxs-lookup"><span data-stu-id="435bc-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="435bc-114">Wenn Sie von mehreren Threads auf eine Vervollständigungs-oder Anforderungs Warteschlange zugreifen müssen, sollte der Zugriff durch einen kritischen Abschnitt, eine schlanke Schreibsperre für Lesevorgänge oder einen ähnlichen Mechanismus koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="435bc-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="435bc-115">Diese Sperrung wird nicht für den Zugriff durch einen einzelnen Thread benötigt.</span><span class="sxs-lookup"><span data-stu-id="435bc-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="435bc-116">Verschiedene Threads können ohne Sperren auf separate Anforderungen/Vervollständigungs Warteschlangen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="435bc-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="435bc-117">Die Synchronisierung ist nur dann erforderlich, wenn mehrere Threads versuchen, auf dieselbe Warteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="435bc-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="435bc-118">Die Synchronisierung ist auch erforderlich, wenn von mehreren Threads im gleichen Socket gesendet und empfangen wird, da die Sende-und Empfangs Vorgänge die Anforderungs Warteschlange des Sockets verwenden.</span><span class="sxs-lookup"><span data-stu-id="435bc-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="435bc-119">Die [**Rio \_ RQ**](riocqueue.md) -TypeDef ist in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="435bc-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="435bc-120">Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="435bc-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="435bc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="435bc-121">Requirements</span></span>



| <span data-ttu-id="435bc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="435bc-122">Requirement</span></span> | <span data-ttu-id="435bc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="435bc-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="435bc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="435bc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="435bc-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="435bc-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="435bc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="435bc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="435bc-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="435bc-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="435bc-128">Header</span><span class="sxs-lookup"><span data-stu-id="435bc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="435bc-129"><dt>Mtausockdef. h (Include mtausock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="435bc-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435bc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="435bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435bc-131">**Riokreaterequestqueue**</span><span class="sxs-lookup"><span data-stu-id="435bc-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="435bc-132">**Rioreceive**</span><span class="sxs-lookup"><span data-stu-id="435bc-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="435bc-133">**Rioreceiveex**</span><span class="sxs-lookup"><span data-stu-id="435bc-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="435bc-134">[**Rioresizerequestqueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="435bc-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="435bc-135">**Randalisend**</span><span class="sxs-lookup"><span data-stu-id="435bc-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="435bc-136">[**Riosendex**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="435bc-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="435bc-137">**Wsasocket**</span><span class="sxs-lookup"><span data-stu-id="435bc-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
