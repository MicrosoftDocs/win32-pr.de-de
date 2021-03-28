---
description: Benachrichtigt eine appbar, dass der Benutzer den Befehl Cascade, Tile horizontal oder Tile vertikal im Kontextmenü der Taskleiste ausgewählt hat.
title: ABN_WINDOWARRANGE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525421"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="ab10a-103">ABN \_ windowarrange-Meldung</span><span class="sxs-lookup"><span data-stu-id="ab10a-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="ab10a-104">Benachrichtigt eine appbar, dass der Benutzer den Befehl Cascade, Tile horizontal oder Tile vertikal im Kontextmenü der Taskleiste ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="ab10a-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ab10a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab10a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab10a-106">*Start*</span><span class="sxs-lookup"><span data-stu-id="ab10a-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="ab10a-107">Ein Flag, das angibt, ob der Cascade-oder Tile-Vorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="ab10a-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="ab10a-108">Dieser Parameter ist **true** , wenn der Vorgang beginnt und die Fenster noch nicht verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="ab10a-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="ab10a-109">Dies ist **false** , wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ab10a-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab10a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab10a-110">Return value</span></span>

<span data-ttu-id="ab10a-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ab10a-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab10a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab10a-112">Remarks</span></span>

<span data-ttu-id="ab10a-113">Das System sendet diese Benachrichtigungs Meldung zunächst zweimal, wobei *LPARAM* auf **true** festgelegt ist, und wenn *LPARAM* auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab10a-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="ab10a-114">Die erste Benachrichtigung wird gesendet, bevor die Fenster kaskadiert oder gekachelt werden, und die zweite Benachrichtigung wird gesendet, nachdem der Cascade-oder Tile-Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ab10a-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab10a-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ab10a-115">Requirements</span></span>



| <span data-ttu-id="ab10a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab10a-116">Requirement</span></span> | <span data-ttu-id="ab10a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ab10a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab10a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab10a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab10a-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab10a-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ab10a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab10a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab10a-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab10a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab10a-122">Header</span><span class="sxs-lookup"><span data-stu-id="ab10a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab10a-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab10a-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




