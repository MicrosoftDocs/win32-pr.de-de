---
title: Iorpcdebugnotify servergetbuffersize-Methode
description: Ruft die RPC-Puffergröße aus dem serverseitigen Debugger ab.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Servergetbuffersize-Methode com
- Servergetbuffersize-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, servergetbuffersize-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957199"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a><span data-ttu-id="ff8e3-106">Iorpcdebugnotify:: servergetbuffersize-Methode</span><span class="sxs-lookup"><span data-stu-id="ff8e3-106">IOrpcDebugNotify::ServerGetBufferSize method</span></span>

<span data-ttu-id="ff8e3-107">Ruft die RPC-Puffergröße aus dem serverseitigen Debugger ab.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-107">Retrieves the RPC buffer size from the server-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="ff8e3-108">Eine Import Bibliothek mit der Funktion **servergetbuffersize** ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-108">An import library containing the **ServerGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ff8e3-109">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ff8e3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff8e3-110">Syntax</span></span>


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="ff8e3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff8e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff8e3-112">*lporpcdebug*</span><span class="sxs-lookup"><span data-stu-id="ff8e3-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="ff8e3-113">Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff8e3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff8e3-114">Return value</span></span>

<span data-ttu-id="ff8e3-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8e3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff8e3-116">Requirements</span></span>



| <span data-ttu-id="ff8e3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff8e3-117">Requirement</span></span> | <span data-ttu-id="ff8e3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ff8e3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ff8e3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff8e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff8e3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff8e3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="ff8e3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff8e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff8e3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff8e3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff8e3-123">Header</span><span class="sxs-lookup"><span data-stu-id="ff8e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff8e3-124"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="ff8e3-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="ff8e3-125">IDL</span><span class="sxs-lookup"><span data-stu-id="ff8e3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff8e3-126"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="ff8e3-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff8e3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff8e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff8e3-128">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ff8e3-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="ff8e3-129">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="ff8e3-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="ff8e3-130">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="ff8e3-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

