---
description: Ruft das Menü Handle für das aktuelle Fenster ab.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: MN_GETHMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216079"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="b1350-103">MN \_ gethmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="b1350-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="b1350-104">Ruft das Menü Handle für das aktuelle Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="b1350-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="b1350-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1350-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1350-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1350-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1350-107">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1350-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b1350-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1350-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1350-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1350-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1350-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1350-110">Return value</span></span>

<span data-ttu-id="b1350-111">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="b1350-111">Type: **HMENU**</span></span>

<span data-ttu-id="b1350-112">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert das **HMENU** für das aktuelle Fenster.</span><span class="sxs-lookup"><span data-stu-id="b1350-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="b1350-113">Wenn dies nicht möglich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="b1350-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1350-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1350-114">Requirements</span></span>



| <span data-ttu-id="b1350-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1350-115">Requirement</span></span> | <span data-ttu-id="b1350-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b1350-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1350-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1350-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1350-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1350-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1350-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1350-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1350-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1350-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1350-121">Header</span><span class="sxs-lookup"><span data-stu-id="b1350-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1350-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b1350-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




