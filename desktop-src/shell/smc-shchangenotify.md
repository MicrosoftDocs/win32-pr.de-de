---
description: Benachrichtigt Sie, dass eine Änderung stattfindet.
title: SMC_SHCHANGENOTIFY Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979801"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="afc8a-103">SMC- \_ shchangenotify-Nachricht</span><span class="sxs-lookup"><span data-stu-id="afc8a-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="afc8a-104">Benachrichtigt Sie, dass eine Änderung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="afc8a-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="afc8a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc8a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc8a-106">*psmc*</span><span class="sxs-lookup"><span data-stu-id="afc8a-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="afc8a-107">Ein Zeiger auf eine [**smcshchangenotifystruct**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) -Struktur mit Informationen zur Änderung.</span><span class="sxs-lookup"><span data-stu-id="afc8a-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc8a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afc8a-108">Return value</span></span>

<span data-ttu-id="afc8a-109">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="afc8a-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc8a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc8a-110">Remarks</span></span>

<span data-ttu-id="afc8a-111">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="afc8a-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc8a-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="afc8a-112">Requirements</span></span>



| <span data-ttu-id="afc8a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc8a-113">Requirement</span></span> | <span data-ttu-id="afc8a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="afc8a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc8a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc8a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="afc8a-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc8a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="afc8a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc8a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="afc8a-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc8a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afc8a-119">Header</span><span class="sxs-lookup"><span data-stu-id="afc8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc8a-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc8a-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="afc8a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="afc8a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afc8a-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afc8a-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




