---
title: Iorpcdebugnotify servernotify-Methode
description: Informiert den Server über eine eingehende Debugger-Anforderung vom Client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Servernotify-Methode com
- Servernotify-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, servernotify-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957149"
---
# <a name="iorpcdebugnotifyservernotify-method"></a><span data-ttu-id="c8c4e-106">Iorpcdebugnotify:: servernotify-Methode</span><span class="sxs-lookup"><span data-stu-id="c8c4e-106">IOrpcDebugNotify::ServerNotify method</span></span>

<span data-ttu-id="c8c4e-107">Informiert den Server über eine eingehende Debugger-Anforderung vom Client.</span><span class="sxs-lookup"><span data-stu-id="c8c4e-107">Informs the server of an incoming debugger request from the client.</span></span>

> [!Note]  
> <span data-ttu-id="c8c4e-108">Eine Import Bibliothek mit der Funktion **servernotify** ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8c4e-108">An import library containing the **ServerNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c8c4e-109">Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8c4e-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c8c4e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8c4e-110">Syntax</span></span>


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="c8c4e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8c4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c4e-112">*lporpcdebug*</span><span class="sxs-lookup"><span data-stu-id="c8c4e-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="c8c4e-113">Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="c8c4e-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c4e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8c4e-114">Return value</span></span>

<span data-ttu-id="c8c4e-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c8c4e-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c4e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8c4e-116">Requirements</span></span>



| <span data-ttu-id="c8c4e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8c4e-117">Requirement</span></span> | <span data-ttu-id="c8c4e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c8c4e-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c8c4e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8c4e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c4e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8c4e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="c8c4e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8c4e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c4e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8c4e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c8c4e-123">Header</span><span class="sxs-lookup"><span data-stu-id="c8c4e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c4e-124"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="c8c4e-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="c8c4e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c8c4e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8c4e-126"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="c8c4e-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8c4e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8c4e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c4e-128">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8c4e-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="c8c4e-129">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="c8c4e-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="c8c4e-130">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="c8c4e-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

