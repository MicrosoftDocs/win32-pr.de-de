---
title: Controls. CurrentPosition
description: Die CurrentPosition-Eigenschaft gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft Sie ab.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. CurrentPosition-Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371712"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="352e7-104">Controls. CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="352e7-104">Controls.currentPosition</span></span>

<span data-ttu-id="352e7-105">Die **CurrentPosition** -Eigenschaft gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="352e7-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="352e7-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="352e7-106">Possible Values</span></span>

<span data-ttu-id="352e7-107">Diese Eigenschaft ist eine Lese-/schreibnummer (**Double**). </span><span class="sxs-lookup"><span data-stu-id="352e7-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="352e7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="352e7-108">Examples</span></span>

<span data-ttu-id="352e7-109">Im folgenden Beispiel wird **CurrentPosition** verwendet, um eine vom Benutzer bereitgestellte Position zu suchen.</span><span class="sxs-lookup"><span data-stu-id="352e7-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="352e7-110">Ein HTML-Schaltflächen Element wird erstellt, um den JScript-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="352e7-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="352e7-111">Ein HTML-Text Eingabe Element namens SetPosition wurde erstellt, um dem Benutzer einen Wert in Sekunden zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="352e7-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="352e7-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="352e7-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="352e7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="352e7-113">Requirements</span></span>



| <span data-ttu-id="352e7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="352e7-114">Requirement</span></span> | <span data-ttu-id="352e7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="352e7-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="352e7-116">Version</span><span class="sxs-lookup"><span data-stu-id="352e7-116">Version</span></span><br/> | <span data-ttu-id="352e7-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="352e7-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="352e7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="352e7-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="352e7-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="352e7-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352e7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="352e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352e7-121">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="352e7-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





