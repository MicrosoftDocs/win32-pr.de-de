---
title: Cdrom. drivespecifier
description: Die drivespecifier-Eigenschaft ruft den CD-oder DVD-Laufwerk Buchstaben ab.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Cdrom. drivespecifier-Fenster Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517522"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="4de54-104">Cdrom. drivespecifier</span><span class="sxs-lookup"><span data-stu-id="4de54-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="4de54-105">Die **drivespecifier** -Eigenschaft ruft den CD-oder DVD-Laufwerk Buchstaben ab.</span><span class="sxs-lookup"><span data-stu-id="4de54-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="4de54-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4de54-106">Possible Values</span></span>

<span data-ttu-id="4de54-107">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="4de54-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de54-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4de54-108">Remarks</span></span>

<span data-ttu-id="4de54-109">In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.</span><span class="sxs-lookup"><span data-stu-id="4de54-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="4de54-110">Diese Eigenschaft ruft einen laufwerkspezifizierer für einen NULL basierten Laufwerks Index innerhalb des mit *cdromcollection* abgerufenen Bereichs ab. **Anzahl**.</span><span class="sxs-lookup"><span data-stu-id="4de54-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="4de54-111">Der abgerufene Wert hat die Form *x*:, wobei *X* den Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="4de54-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="4de54-112">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4de54-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="4de54-113">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4de54-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4de54-114">**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4de54-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="4de54-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4de54-115">Examples</span></span>

<span data-ttu-id="4de54-116">Im folgenden JScript-Beispiel wird *CDROM* verwendet. **drivespecifier** zum Ausfüllen eines HTML-Text Bereichs namens MyText mit einer durch Trennzeichen getrennten Liste von verfügbaren CD-und DVD-Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="4de54-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="4de54-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4de54-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="4de54-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4de54-118">Requirements</span></span>



| <span data-ttu-id="4de54-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4de54-119">Requirement</span></span> | <span data-ttu-id="4de54-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4de54-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4de54-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4de54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4de54-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4de54-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4de54-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4de54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4de54-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4de54-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4de54-125">Version</span><span class="sxs-lookup"><span data-stu-id="4de54-125">Version</span></span><br/>                  | <span data-ttu-id="4de54-126">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4de54-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="4de54-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4de54-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de54-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de54-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de54-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4de54-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de54-130">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4de54-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="4de54-131">**Cdromcollection. Count**</span><span class="sxs-lookup"><span data-stu-id="4de54-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="4de54-132">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="4de54-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4de54-133">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="4de54-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





