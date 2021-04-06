---
title: Iorpcdebugnotify clientfillbuffer-Methode
description: Sendet Daten vom Client Debugger an den Server Debugger.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Clientfillbuffer-Methode com
- Clientfillbuffer-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, clientfillbuffer-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743705"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="1d036-106">Iorpcdebugnotify:: clientfillbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="1d036-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="1d036-107">Sendet Daten vom Client Debugger an den Server Debugger.</span><span class="sxs-lookup"><span data-stu-id="1d036-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="1d036-108">Eine Import Bibliothek mit der Funktion " **clientfillbuffer** " ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d036-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1d036-109">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d036-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1d036-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d036-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="1d036-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d036-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d036-112">*lporpcdebug*</span><span class="sxs-lookup"><span data-stu-id="1d036-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="1d036-113">Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="1d036-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d036-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d036-114">Return value</span></span>

<span data-ttu-id="1d036-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1d036-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d036-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d036-116">Requirements</span></span>



| <span data-ttu-id="1d036-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d036-117">Requirement</span></span> | <span data-ttu-id="1d036-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1d036-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1d036-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d036-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d036-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d036-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="1d036-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d036-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d036-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d036-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1d036-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d036-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d036-124"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="1d036-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="1d036-125">IDL</span><span class="sxs-lookup"><span data-stu-id="1d036-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d036-126"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="1d036-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d036-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d036-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d036-128">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="1d036-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="1d036-129">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="1d036-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

