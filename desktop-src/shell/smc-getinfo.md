---
description: Fordert Informationen über ein reguläres Menü Element an.
title: SMC_GETINFO Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994839"
---
# <a name="smc_getinfo-message"></a><span data-ttu-id="7a3bf-103">SMC- \_ GetInfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7a3bf-103">SMC\_GETINFO message</span></span>

<span data-ttu-id="7a3bf-104">Fordert Informationen über ein reguläres Menü Element an.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-104">Requests information about a regular menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="7a3bf-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a3bf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a3bf-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="7a3bf-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7a3bf-107">Ein Zeiger auf eine [**sminfo**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-107">A pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="7a3bf-108">Füllen Sie die Struktur mit den entsprechenden Informationen aus, und geben Sie \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a3bf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a3bf-109">Return value</span></span>

<span data-ttu-id="7a3bf-110">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="7a3bf-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a3bf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a3bf-111">Remarks</span></span>

<span data-ttu-id="7a3bf-112">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3bf-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7a3bf-113">Requirements</span></span>



| <span data-ttu-id="7a3bf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a3bf-114">Requirement</span></span> | <span data-ttu-id="7a3bf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3bf-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3bf-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a3bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a3bf-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a3bf-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7a3bf-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a3bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7a3bf-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a3bf-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a3bf-120">Header</span><span class="sxs-lookup"><span data-stu-id="7a3bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a3bf-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a3bf-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a3bf-122">IDL</span><span class="sxs-lookup"><span data-stu-id="7a3bf-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a3bf-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a3bf-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




