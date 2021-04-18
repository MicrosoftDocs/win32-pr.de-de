---
title: Network. framesskipped
description: Die framesskipped-Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Netzwerk. framesskipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365491"
---
# <a name="networkframesskipped"></a><span data-ttu-id="d3626-104">Network. framesskipped</span><span class="sxs-lookup"><span data-stu-id="d3626-104">Network.framesSkipped</span></span>

<span data-ttu-id="d3626-105">Die **framesskipped** -Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.</span><span class="sxs-lookup"><span data-stu-id="d3626-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3626-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3626-106">Syntax</span></span>

<span data-ttu-id="d3626-107">*Player*. *Netzwerk*. **framesskipped**</span><span class="sxs-lookup"><span data-stu-id="d3626-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d3626-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d3626-108">Possible Values</span></span>

<span data-ttu-id="d3626-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="d3626-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="d3626-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3626-110">Examples</span></span>

<span data-ttu-id="d3626-111">Im folgenden JScript-Beispiel wird *Network* verwendet. **framesskipped** zum Anzeigen der Gesamtzahl der Rahmen, die während der Wiedergabe ausgelassen werden, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="d3626-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="d3626-112">Die Informationen werden in einem HTML-div-Code angezeigt, der mit ID = "FS" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3626-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="d3626-113">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d3626-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="d3626-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3626-114">Requirements</span></span>



| <span data-ttu-id="d3626-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3626-115">Requirement</span></span> | <span data-ttu-id="d3626-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d3626-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3626-117">Version</span><span class="sxs-lookup"><span data-stu-id="d3626-117">Version</span></span><br/> | <span data-ttu-id="d3626-118">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d3626-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d3626-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d3626-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3626-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3626-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3626-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3626-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3626-122">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="d3626-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





