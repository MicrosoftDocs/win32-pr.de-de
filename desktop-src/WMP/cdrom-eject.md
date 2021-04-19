---
title: Cdrom. eject-Methode
description: Die Auswerfen-Methode fügt die CD oder DVD vom Laufwerk ein. | Cdrom. eject-Methode
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Auswerfen-Methode, Windows-Media Player
- Auswerfen-Methode, Windows Media Player, cdrom-Klasse
- Cdrom-Klasse, Windows Media Player, Auswerfen-Methode
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363922"
---
# <a name="cdromeject-method"></a><span data-ttu-id="e944b-107">Cdrom. eject-Methode</span><span class="sxs-lookup"><span data-stu-id="e944b-107">Cdrom.eject method</span></span>

<span data-ttu-id="e944b-108">Die **auswerfen** -Methode fügt die CD oder DVD vom Laufwerk ein.</span><span class="sxs-lookup"><span data-stu-id="e944b-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e944b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e944b-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="e944b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e944b-110">Parameters</span></span>

<span data-ttu-id="e944b-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e944b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e944b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e944b-112">Return value</span></span>

<span data-ttu-id="e944b-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e944b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e944b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e944b-114">Remarks</span></span>

<span data-ttu-id="e944b-115">Wenn die Laufwerks Tür geöffnet ist, schließt diese Methode die Tür.</span><span class="sxs-lookup"><span data-stu-id="e944b-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="e944b-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e944b-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e944b-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e944b-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e944b-118">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e944b-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e944b-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e944b-119">Examples</span></span>

<span data-ttu-id="e944b-120">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das *CDROM* verwendet. **auswerfen** zum Öffnen der Tür des Laufwerks mit dem laufwerkspezifizierer Index NULL.</span><span class="sxs-lookup"><span data-stu-id="e944b-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="e944b-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e944b-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="e944b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e944b-122">Requirements</span></span>



| <span data-ttu-id="e944b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e944b-123">Requirement</span></span> | <span data-ttu-id="e944b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e944b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e944b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e944b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e944b-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e944b-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e944b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e944b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e944b-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e944b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e944b-129">Version</span><span class="sxs-lookup"><span data-stu-id="e944b-129">Version</span></span><br/>                  | <span data-ttu-id="e944b-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e944b-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e944b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e944b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e944b-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e944b-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e944b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e944b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e944b-134">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e944b-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="e944b-135">**Player. playstate**</span><span class="sxs-lookup"><span data-stu-id="e944b-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="e944b-136">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e944b-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e944b-137">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e944b-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





