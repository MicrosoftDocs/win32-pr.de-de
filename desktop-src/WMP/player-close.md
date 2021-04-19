---
title: Player. Close-Methode
description: Die Close-Methode gibt Windows Media Player-Ressourcen frei.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Schließen von Methoden Fenstern Media Player
- Close-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, Close-Methode
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358620"
---
# <a name="playerclose-method"></a><span data-ttu-id="6bb44-106">Player. Close-Methode</span><span class="sxs-lookup"><span data-stu-id="6bb44-106">Player.close method</span></span>

<span data-ttu-id="6bb44-107">Die **Close** -Methode gibt Windows Media Player-Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="6bb44-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bb44-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="6bb44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bb44-109">Parameters</span></span>

<span data-ttu-id="6bb44-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6bb44-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bb44-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bb44-111">Return value</span></span>

<span data-ttu-id="6bb44-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6bb44-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb44-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bb44-113">Remarks</span></span>

<span data-ttu-id="6bb44-114">Diese Methode schließt die aktuelle digitale Mediendatei, nicht Windows Media Player selbst.</span><span class="sxs-lookup"><span data-stu-id="6bb44-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="6bb44-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bb44-115">Examples</span></span>

<span data-ttu-id="6bb44-116">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das beim Klicken auf die Wiedergabe in Windows-Media Player beendet und die verwendeten Ressourcen freigibt.</span><span class="sxs-lookup"><span data-stu-id="6bb44-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="6bb44-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bb44-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="6bb44-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb44-118">Requirements</span></span>



| <span data-ttu-id="6bb44-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bb44-119">Requirement</span></span> | <span data-ttu-id="6bb44-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6bb44-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb44-121">Version</span><span class="sxs-lookup"><span data-stu-id="6bb44-121">Version</span></span><br/> | <span data-ttu-id="6bb44-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6bb44-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6bb44-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb44-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bb44-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb44-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb44-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bb44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb44-126">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="6bb44-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





