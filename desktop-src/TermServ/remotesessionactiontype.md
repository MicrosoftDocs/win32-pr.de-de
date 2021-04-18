---
title: Remotesessionaktionstyp-Enumeration
description: Wird verwendet, um den Typ der Remote Aktion anzugeben.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Remotesessionaktionstyp-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340318"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="b9a55-104">Remotesessionaktionstyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b9a55-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="b9a55-105">Wird verwendet, um den Typ der Remote Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b9a55-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a55-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9a55-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="b9a55-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b9a55-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b9a55-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**Remotesessionaktionszeichen**</span><span class="sxs-lookup"><span data-stu-id="b9a55-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-109">Zeigt die Charms in der Remote Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="b9a55-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="b9a55-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**Remotesessionaktionsleiste**</span><span class="sxs-lookup"><span data-stu-id="b9a55-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-111">Hiermit wird die APP-Leiste in der Remote Sitzung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9a55-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="b9a55-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**Remotesessionaktionssnap**</span><span class="sxs-lookup"><span data-stu-id="b9a55-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-113">Dockt die Anwendung in der Remote Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="b9a55-113">Docks the application in the remote session.</span></span> <span data-ttu-id="b9a55-114">Diese Option wurde als veraltet markiert und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9a55-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="b9a55-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**Remotesessionaction Startscreen**</span><span class="sxs-lookup"><span data-stu-id="b9a55-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-116">Bewirkt, dass der Startbildschirm in der Remote Sitzung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a55-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="b9a55-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**Remotesessionaktionsswitch**</span><span class="sxs-lookup"><span data-stu-id="b9a55-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-118">Bewirkt, dass das Fenster "Anwendungs Switch" in der Remote Sitzung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a55-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="b9a55-119">Dies ist das gleiche wie beim Drücken von Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="b9a55-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="b9a55-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**Remotesessionaktionscenter**</span><span class="sxs-lookup"><span data-stu-id="b9a55-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="b9a55-121">Bewirkt, dass das Aktions Center in der Remote Sitzung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a55-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="b9a55-122">Dies entspricht dem Benutzer, der "Win + A" drückt.</span><span class="sxs-lookup"><span data-stu-id="b9a55-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="b9a55-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 und Windows 8:** Dieser Wert wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9a55-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9a55-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9a55-124">Requirements</span></span>



| <span data-ttu-id="b9a55-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9a55-125">Requirement</span></span> | <span data-ttu-id="b9a55-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b9a55-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a55-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9a55-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a55-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b9a55-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="b9a55-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9a55-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a55-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9a55-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="b9a55-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b9a55-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9a55-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9a55-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9a55-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9a55-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a55-134">**IMsRdpClient8:: sendremoteaction**</span><span class="sxs-lookup"><span data-stu-id="b9a55-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





