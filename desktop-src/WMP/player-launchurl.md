---
title: Player. launchurl-Methode
description: Die launchurl-Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. | Player. launchurl-Methode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- launchurl-Methode, Windows Media Player
- launchurl-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, launchurl-Methode
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359281"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="64681-107">Player. launchurl-Methode</span><span class="sxs-lookup"><span data-stu-id="64681-107">Player.launchURL method</span></span>

<span data-ttu-id="64681-108">Die **launchurl** -Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64681-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="64681-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="64681-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="64681-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64681-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64681-111">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64681-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64681-112">**Zeichen** folgen Wert, der die zu startende URL darstellt.</span><span class="sxs-lookup"><span data-stu-id="64681-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64681-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64681-113">Return value</span></span>

<span data-ttu-id="64681-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64681-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64681-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64681-115">Remarks</span></span>

<span data-ttu-id="64681-116">Diese Methode öffnet nur Webseiten mithilfe der http-oder HTTPS-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="64681-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="64681-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64681-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="64681-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64681-118">Examples</span></span>

<span data-ttu-id="64681-119">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das, wenn darauf geklickt wird, die Microsoft-Website in einem neuen Browserfenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64681-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="64681-120">Das **Player** -Element wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="64681-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="64681-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64681-121">Requirements</span></span>



| <span data-ttu-id="64681-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64681-122">Requirement</span></span> | <span data-ttu-id="64681-123">Wert</span><span class="sxs-lookup"><span data-stu-id="64681-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64681-124">Version</span><span class="sxs-lookup"><span data-stu-id="64681-124">Version</span></span><br/> | <span data-ttu-id="64681-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="64681-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="64681-126">DLL</span><span class="sxs-lookup"><span data-stu-id="64681-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="64681-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64681-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64681-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64681-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64681-129">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="64681-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





