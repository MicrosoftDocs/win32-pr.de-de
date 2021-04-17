---
title: Iorpcdebug bugnotify-Schnittstelle
description: Bietet Remotedebugfunktionen.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Iorpcdebug-Schnittstelle com
- Iorpcdebug-Schnittstelle com, beschrieben
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519055"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="bafec-105">Iorpcdebug bugnotify-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bafec-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="bafec-106">Bietet Remotedebugfunktionen.</span><span class="sxs-lookup"><span data-stu-id="bafec-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="bafec-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="bafec-107">When to implement</span></span>

<span data-ttu-id="bafec-108">Implementieren Sie diese Schnittstelle, um Remote Debugging über RPC zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bafec-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bafec-109">Verwendung</span><span class="sxs-lookup"><span data-stu-id="bafec-109">When to use</span></span>

<span data-ttu-id="bafec-110">Diese Schnittstelle sollte für das Prozess interne Remote Debuggen verwendet werden, wenn für die com-Debugger-Benachrichtigungen keine Software Ausnahmen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bafec-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="bafec-111">Sie ermöglicht es, in-Process-Debuggern durch direkte Aufrufe mithilfe dieser Methoden benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="bafec-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="bafec-112">Member</span><span class="sxs-lookup"><span data-stu-id="bafec-112">Members</span></span>

<span data-ttu-id="bafec-113">Die Schnittstelle **iorpcdebug bugnotify** erbt von der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bafec-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bafec-114">" **Iorpcdebug bugnotify** " verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bafec-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="bafec-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="bafec-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bafec-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="bafec-116">Methods</span></span>

<span data-ttu-id="bafec-117">Die **iorpcdebugnotify** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bafec-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="bafec-118">Methode</span><span class="sxs-lookup"><span data-stu-id="bafec-118">Method</span></span>                                                              | <span data-ttu-id="bafec-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bafec-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="bafec-120">**Clientfillbuffer**</span><span class="sxs-lookup"><span data-stu-id="bafec-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="bafec-121">Sendet Daten vom Client Debugger an den Server Debugger.</span><span class="sxs-lookup"><span data-stu-id="bafec-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="bafec-122">**Clientgetbuffersize**</span><span class="sxs-lookup"><span data-stu-id="bafec-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="bafec-123">Ruft die RPC-Puffergröße aus dem Client seitigen Debugger ab.</span><span class="sxs-lookup"><span data-stu-id="bafec-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="bafec-124">**Clientnotify**</span><span class="sxs-lookup"><span data-stu-id="bafec-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="bafec-125">Informiert den Client über eine ausgehende Debugger-Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="bafec-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="bafec-126">**Serverfillbuffer**</span><span class="sxs-lookup"><span data-stu-id="bafec-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="bafec-127">Sendet Daten vom Server Debugger an den Client Debugger.</span><span class="sxs-lookup"><span data-stu-id="bafec-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="bafec-128">**Servergetbuffersize**</span><span class="sxs-lookup"><span data-stu-id="bafec-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="bafec-129">Ruft die RPC-Puffergröße aus dem serverseitigen Debugger ab.</span><span class="sxs-lookup"><span data-stu-id="bafec-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="bafec-130">**Servernotify**</span><span class="sxs-lookup"><span data-stu-id="bafec-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="bafec-131">Informiert den Server über eine eingehende Debugger-Anforderung vom Client.</span><span class="sxs-lookup"><span data-stu-id="bafec-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bafec-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bafec-132">Remarks</span></span>

<span data-ttu-id="bafec-133">Eine Import Bibliothek mit der **iorpcdebugnotify** -Schnittstelle ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="bafec-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bafec-134">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Methoden über die **iorpcdebugnotify** -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bafec-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bafec-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bafec-135">Requirements</span></span>



| <span data-ttu-id="bafec-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bafec-136">Requirement</span></span> | <span data-ttu-id="bafec-137">Wert</span><span class="sxs-lookup"><span data-stu-id="bafec-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bafec-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bafec-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bafec-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bafec-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="bafec-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bafec-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bafec-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bafec-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bafec-142">Header</span><span class="sxs-lookup"><span data-stu-id="bafec-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bafec-143"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="bafec-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="bafec-144">IDL</span><span class="sxs-lookup"><span data-stu-id="bafec-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bafec-145"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="bafec-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bafec-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bafec-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafec-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="bafec-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="bafec-148">**ORPC \_ dbg \_ alle**</span><span class="sxs-lookup"><span data-stu-id="bafec-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="bafec-149">**ORPC \_ dbg- \_ Puffer**</span><span class="sxs-lookup"><span data-stu-id="bafec-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="bafec-150">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bafec-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="bafec-151">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="bafec-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

