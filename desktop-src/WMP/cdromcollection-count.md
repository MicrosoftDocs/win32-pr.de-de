---
title: Cdromcollection. Count
description: Die Count-Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Cdromcollection. count-Windows-Media Player
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371338"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="874d8-104">Cdromcollection. Count</span><span class="sxs-lookup"><span data-stu-id="874d8-104">CdromCollection.count</span></span>

<span data-ttu-id="874d8-105">Die **count** -Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.</span><span class="sxs-lookup"><span data-stu-id="874d8-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="874d8-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="874d8-106">Possible Values</span></span>

<span data-ttu-id="874d8-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="874d8-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="874d8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="874d8-108">Remarks</span></span>

<span data-ttu-id="874d8-109">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="874d8-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="874d8-110">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="874d8-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="874d8-111">DVD-ROM-Laufwerke werden genau wie CD-Laufwerke gezählt.</span><span class="sxs-lookup"><span data-stu-id="874d8-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="874d8-112">Das Windows Media Player-Steuerelement unterstützt jedoch nur DVD-Funktionen für Windows XP oder höhere Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="874d8-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="874d8-113">In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.</span><span class="sxs-lookup"><span data-stu-id="874d8-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="874d8-114">**Windows Media Player 10 Mobile:** Diese Methode gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="874d8-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="874d8-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="874d8-115">Examples</span></span>

<span data-ttu-id="874d8-116">Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **Anzahl, um** die Anzahl der CD-und DVD-Laufwerke anzuzeigen, die auf dem Computer des Benutzers verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="874d8-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="874d8-117">Das Player-Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="874d8-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="874d8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="874d8-118">Requirements</span></span>



| <span data-ttu-id="874d8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="874d8-119">Requirement</span></span> | <span data-ttu-id="874d8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="874d8-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="874d8-121">Version</span><span class="sxs-lookup"><span data-stu-id="874d8-121">Version</span></span><br/> | <span data-ttu-id="874d8-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="874d8-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="874d8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="874d8-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="874d8-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="874d8-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="874d8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="874d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874d8-126">**Cdromcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="874d8-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="874d8-127">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="874d8-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="874d8-128">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="874d8-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





