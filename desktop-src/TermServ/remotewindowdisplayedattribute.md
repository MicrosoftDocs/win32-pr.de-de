---
title: Remotewindowdisplayedattribute-Enumeration
description: Wird mit der-Methode verwendet, um Informationen zum Ereignis anzugeben.
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- Remotewindowdisplayedattribute-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342844"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a><span data-ttu-id="64188-104">Remotewindowdisplayedattribute-Enumeration</span><span class="sxs-lookup"><span data-stu-id="64188-104">RemoteWindowDisplayedAttribute enumeration</span></span>

<span data-ttu-id="64188-105">Wird mit der-Methode verwendet, um Informationen zum Ereignis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64188-105">Used with the method to specify information about the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="64188-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64188-106">Syntax</span></span>


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a><span data-ttu-id="64188-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="64188-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="64188-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteappwindownone**</span><span class="sxs-lookup"><span data-stu-id="64188-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="64188-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteappwindowangezeigte**</span><span class="sxs-lookup"><span data-stu-id="64188-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="64188-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteappshellicondisplayed**</span><span class="sxs-lookup"><span data-stu-id="64188-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span></span>
<span data-ttu-id="64188-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="64188-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="64188-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64188-112">Requirements</span></span>



| <span data-ttu-id="64188-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64188-113">Requirement</span></span> | <span data-ttu-id="64188-114">Wert</span><span class="sxs-lookup"><span data-stu-id="64188-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64188-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64188-115">Minimum supported client</span></span><br/> | <span data-ttu-id="64188-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="64188-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="64188-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64188-117">Minimum supported server</span></span><br/> | <span data-ttu-id="64188-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64188-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="64188-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="64188-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="64188-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64188-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64188-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64188-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64188-122">**"Onremotewindow" angezeigt**</span><span class="sxs-lookup"><span data-stu-id="64188-122">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





