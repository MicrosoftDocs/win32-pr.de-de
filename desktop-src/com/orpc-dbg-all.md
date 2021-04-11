---
title: ORPC_DBG_ALL Struktur
description: Die ORPC \_ dbg \_ all-Struktur wird verwendet, um Parameter an die Methoden der iorpcdebugnotify-Schnittstelle zu übergeben.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM für ORPC_DBG_ALL Struktur
- LPORPC_DBG_ALL Struktur Zeiger com
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103259"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="4b968-105">ORPC \_ dbg \_ all-Struktur</span><span class="sxs-lookup"><span data-stu-id="4b968-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="4b968-106">Die **ORPC \_ dbg \_ all** -Struktur wird verwendet, um Parameter an die Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4b968-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="4b968-107">Jede Methode der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet eine andere Kombination der nachfolgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="4b968-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="4b968-108">Wenn ein Member nicht als von einer Methode verwendet angegeben wird, ist er nicht definiert, wenn er an diese Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4b968-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b968-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b968-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="4b968-110">Member</span><span class="sxs-lookup"><span data-stu-id="4b968-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b968-111">**psignature**</span><span class="sxs-lookup"><span data-stu-id="4b968-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-112">Ein Zeiger auf einen **Byte** Puffer, der Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="4b968-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="4b968-113">Die ersten vier Bytes: die ASCII-Zeichen "Marb" in zunehmender Speicher Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b968-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="4b968-114">Nächste 16 Bytes: eine **GUID** , die die aufgerufene Benachrichtigung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4b968-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="4b968-115">Sie enthält eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="4b968-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="4b968-116">[**Clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md): 9ed14f 80-9673-101A-b07b-00dd01113f</span><span class="sxs-lookup"><span data-stu-id="4b968-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="4b968-117">[**Clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101 a-B07B-00dd01113f 11</span><span class="sxs-lookup"><span data-stu-id="4b968-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="4b968-118">[**Clientnotify**](iorpcdebugnotify-clientnotify.md): 4b60e540-9674-101A-b07b-00dd01113f</span><span class="sxs-lookup"><span data-stu-id="4b968-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="4b968-119">[**Servernotify**](iorpcdebugnotify-servernotify.md): 1084fa00-9674-101A-b07b-00dd01113voll ständig verfügbar</span><span class="sxs-lookup"><span data-stu-id="4b968-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="4b968-120">[**Servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-b07b-00dd01113f</span><span class="sxs-lookup"><span data-stu-id="4b968-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="4b968-121">[**Serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md): 2fc09500-9674-101A-b07b-00dd01113f</span><span class="sxs-lookup"><span data-stu-id="4b968-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="4b968-122">Nächste vier Bytes: für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4b968-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-123">Wird von allen Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="4b968-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-125">Ein Zeiger auf eine [**rpcolemess**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) -Struktur, die Informationen zu RPC-Daten Marshalling enthält.</span><span class="sxs-lookup"><span data-stu-id="4b968-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-126">Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md), [**clientnotify**](iorpcdebugnotify-clientnotify.md), [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md), [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)und [**servernotify**](iorpcdebugnotify-servernotify.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-127">**REFIID**</span><span class="sxs-lookup"><span data-stu-id="4b968-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-128">Ein Zeiger auf die IID der [**iorpcdebug**](iorpcdebugnotify.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4b968-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-129">Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md), [**clientnotify**](iorpcdebugnotify-clientnotify.md), [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md), [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)und [**servernotify**](iorpcdebugnotify-servernotify.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="4b968-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-131">Ein Zeiger auf die Schnittstelle " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) " der com-RPC-Kanal Implementierung auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="4b968-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-132">Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-133">**punkproxymgr**</span><span class="sxs-lookup"><span data-stu-id="4b968-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-134">Ein Zeiger auf die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle des Objekts, das an diesem Debugger-Aufruf beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="4b968-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="4b968-135">Kann **null** sein. Dadurch wird jedoch die Debugger-Funktionalität reduziert.</span><span class="sxs-lookup"><span data-stu-id="4b968-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-136">Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md)und [**clientnotify**](iorpcdebugnotify-clientnotify.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-137">**pinterface**</span><span class="sxs-lookup"><span data-stu-id="4b968-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-138">Ein Zeiger auf die COM-Schnittstelle der Methode, die von diesem RPC aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4b968-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="4b968-139">Darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4b968-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-140">Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-141">**pUnkObject**</span><span class="sxs-lookup"><span data-stu-id="4b968-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-142">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4b968-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-143">Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-144">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b968-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-145">Der Zweck dieses Members ändert sich für jede der folgenden Benachrichtigungen:</span><span class="sxs-lookup"><span data-stu-id="4b968-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="4b968-146">[**Clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md): die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="4b968-147">Wenn der Wert NULL ist, müssen keine Informationen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="4b968-148">[**Clientnotify**](iorpcdebugnotify-clientnotify.md): das **HRESULT** des letzten RPC.</span><span class="sxs-lookup"><span data-stu-id="4b968-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="4b968-149">[**Servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md): die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="4b968-150">Wenn der Wert NULL ist, müssen keine Informationen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-151">Wird von der [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-und [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-152">**umschließt**</span><span class="sxs-lookup"><span data-stu-id="4b968-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-153">Ein Zeiger auf eine [**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md) Struktur, die die per RPC gemarshallte Debuginformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="4b968-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="4b968-154">Ist nicht definiert, wenn **cbbuffer** NULL ist.</span><span class="sxs-lookup"><span data-stu-id="4b968-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-155">Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-, [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-156">**cbbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b968-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-157">Die Länge (in Byte) der Daten, auf die von **pvbuffer** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4b968-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-158">Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-, [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-159">**lpcbbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b968-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-160">Die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="4b968-161">Wenn der Wert NULL ist, müssen keine Informationen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="4b968-162">Dieser Wert ersetzt den Wert, der in **HRESULT** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b968-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="4b968-163">Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-Methode, der [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b968-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b968-164">**bleiben**</span><span class="sxs-lookup"><span data-stu-id="4b968-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="4b968-165">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4b968-165">Reserved.</span></span> <span data-ttu-id="4b968-166">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b968-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b968-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b968-167">Requirements</span></span>



| <span data-ttu-id="4b968-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b968-168">Requirement</span></span> | <span data-ttu-id="4b968-169">Wert</span><span class="sxs-lookup"><span data-stu-id="4b968-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4b968-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b968-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4b968-171">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b968-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="4b968-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b968-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4b968-173">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b968-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4b968-174">Header</span><span class="sxs-lookup"><span data-stu-id="4b968-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b968-175"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="4b968-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b968-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b968-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b968-177">**ORPC \_ dbg- \_ Puffer**</span><span class="sxs-lookup"><span data-stu-id="4b968-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="4b968-178">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b968-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="4b968-179">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="4b968-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="4b968-180">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="4b968-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

