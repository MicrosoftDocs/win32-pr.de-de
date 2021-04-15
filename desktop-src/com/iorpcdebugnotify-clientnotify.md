---
title: Iorpcdebugnotify clientnotify-Methode
description: Informiert den Client über eine ausgehende Debugger-Anforderung an den Server.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Clientnotify-Methode com
- Clientnotify-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, clientnotify-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479191"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a><span data-ttu-id="55564-106">Iorpcdebugnotify:: clientnotify-Methode</span><span class="sxs-lookup"><span data-stu-id="55564-106">IOrpcDebugNotify::ClientNotify method</span></span>

<span data-ttu-id="55564-107">Informiert den Client über eine ausgehende Debugger-Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="55564-107">Informs the client of an outgoing debugger request to the server.</span></span>

> [!Note]  
> <span data-ttu-id="55564-108">Eine Import Bibliothek mit der Funktion **clientnotify** ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="55564-108">An import library containing the **ClientNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="55564-109">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="55564-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="55564-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="55564-110">Syntax</span></span>


```C++
void ClientNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="55564-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="55564-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55564-112">*lporpcdebug*</span><span class="sxs-lookup"><span data-stu-id="55564-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="55564-113">Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="55564-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55564-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55564-114">Return value</span></span>

<span data-ttu-id="55564-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="55564-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="55564-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55564-116">Requirements</span></span>



| <span data-ttu-id="55564-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55564-117">Requirement</span></span> | <span data-ttu-id="55564-118">Wert</span><span class="sxs-lookup"><span data-stu-id="55564-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="55564-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55564-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55564-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55564-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="55564-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55564-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55564-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55564-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55564-123">Header</span><span class="sxs-lookup"><span data-stu-id="55564-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55564-124"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="55564-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="55564-125">IDL</span><span class="sxs-lookup"><span data-stu-id="55564-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55564-126"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="55564-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55564-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55564-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55564-128">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55564-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="55564-129">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="55564-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="55564-130">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="55564-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

