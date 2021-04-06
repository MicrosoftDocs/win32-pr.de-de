---
title: Iorpcdebugnotify serverfillbuffer-Methode
description: Sendet Daten vom Server Debugger an den Client Debugger.
ms.assetid: 58813f28-6e32-478c-8b12-8cf0ebe01973
keywords:
- Serverfillbuffer-Methode com
- Serverfillbuffer-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, serverfillbuffer-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffac861e3ac2d35d6d738755e2e5d7814ec41b4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743704"
---
# <a name="iorpcdebugnotifyserverfillbuffer-method"></a><span data-ttu-id="fade6-106">Iorpcdebugnotify:: serverfillbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="fade6-106">IOrpcDebugNotify::ServerFillBuffer method</span></span>

<span data-ttu-id="fade6-107">Sendet Daten vom Server Debugger an den Client Debugger.</span><span class="sxs-lookup"><span data-stu-id="fade6-107">Sends data from the server debugger to the client debugger.</span></span>

> [!Note]  
> <span data-ttu-id="fade6-108">Eine Import Bibliothek mit der Funktion **serverfillbuffer** ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="fade6-108">An import library containing the **ServerFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fade6-109">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fade6-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fade6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fade6-110">Syntax</span></span>


```C++
void ServerFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="fade6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fade6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fade6-112">*lporpcdebug*</span><span class="sxs-lookup"><span data-stu-id="fade6-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="fade6-113">Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="fade6-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fade6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fade6-114">Return value</span></span>

<span data-ttu-id="fade6-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fade6-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fade6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fade6-116">Requirements</span></span>



| <span data-ttu-id="fade6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fade6-117">Requirement</span></span> | <span data-ttu-id="fade6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fade6-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fade6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fade6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fade6-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fade6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="fade6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fade6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fade6-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fade6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fade6-123">Header</span><span class="sxs-lookup"><span data-stu-id="fade6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fade6-124"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="fade6-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="fade6-125">IDL</span><span class="sxs-lookup"><span data-stu-id="fade6-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fade6-126"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="fade6-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fade6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fade6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fade6-128">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fade6-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="fade6-129">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="fade6-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="fade6-130">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="fade6-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

