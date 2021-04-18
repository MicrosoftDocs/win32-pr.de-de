---
title: Controls. currentpositionstring
description: Die currentpositionstring-Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh mm SS (Stunden, Minuten und Sekunden) formatiert ist.
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls. currentpositionstring Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371490"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="388fe-104">Controls. currentpositionstring</span><span class="sxs-lookup"><span data-stu-id="388fe-104">Controls.currentPositionString</span></span>

<span data-ttu-id="388fe-105">Die **currentpositionstring** -Eigenschaft ruft die aktuelle Position im Medien Element als **Zeichen** Folge ab, die als hh: mm: SS (Stunden, Minuten und Sekunden) formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="388fe-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="388fe-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="388fe-106">Possible Values</span></span>

<span data-ttu-id="388fe-107">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="388fe-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="388fe-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="388fe-108">Remarks</span></span>

<span data-ttu-id="388fe-109">Wenn das Medien Element weniger als eine Stunde lang ist, wird der HH:-Teil nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="388fe-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="388fe-110">Sie sollten Code einschließen, um den Timer zu beenden, wenn das Medien Element beendet oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="388fe-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="388fe-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="388fe-111">Examples</span></span>

<span data-ttu-id="388fe-112">Im folgenden JScript-Beispiel wird ein HTML-Timer gestartet, der die aktuelle Position der Mediendatei in Intervallen von einer Sekunde anzeigt.</span><span class="sxs-lookup"><span data-stu-id="388fe-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="388fe-113">Ein HTML-Textelement mit dem Namen MyText wurde erstellt, um die aktuelle Position anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="388fe-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="388fe-114">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="388fe-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="388fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="388fe-115">Requirements</span></span>



| <span data-ttu-id="388fe-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="388fe-116">Requirement</span></span> | <span data-ttu-id="388fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="388fe-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="388fe-118">Version</span><span class="sxs-lookup"><span data-stu-id="388fe-118">Version</span></span><br/> | <span data-ttu-id="388fe-119">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="388fe-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="388fe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="388fe-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="388fe-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="388fe-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388fe-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="388fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388fe-123">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="388fe-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





