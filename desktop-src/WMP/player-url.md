---
title: Player. URL
description: Die URL-Eigenschaft gibt den Namen des zu Wiedergabe enden Medien Elements an oder ruft ihn ab.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372336"
---
# <a name="playerurl"></a><span data-ttu-id="1512e-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="1512e-104">Player.URL</span></span>

<span data-ttu-id="1512e-105">Die **URL** -Eigenschaft gibt den Namen des zu Wiedergabe enden Medien Elements an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="1512e-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="1512e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1512e-106">Syntax</span></span>

<span data-ttu-id="1512e-107">*Player* . **URL**</span><span class="sxs-lookup"><span data-stu-id="1512e-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1512e-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1512e-108">Possible Values</span></span>

<span data-ttu-id="1512e-109">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge** ohne Standardwert.</span><span class="sxs-lookup"><span data-stu-id="1512e-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1512e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1512e-110">Remarks</span></span>

<span data-ttu-id="1512e-111">Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch ist oder weniger restriktiv ist als die Sicherheitszone des aufrufenden Programms oder der Webseite.</span><span class="sxs-lookup"><span data-stu-id="1512e-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="1512e-112">Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse anstelle der IP-Adresse mit dem DNS-Namen (Domain Nameserver) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1512e-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="1512e-113">Diese Methode kann nicht aus dem Ereignishandlercode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1512e-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="1512e-114">Aufruf *Player*. Die **URL** eines Ereignis Handlers kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="1512e-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="1512e-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1512e-115">Examples</span></span>

<span data-ttu-id="1512e-116">Im folgenden Beispiel werden ein HTML-Text Eingabe Element und ein HTML-Schaltflächen-Eingabe Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="1512e-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="1512e-117">Mit dem Text-Element kann der Benutzer einen Pfad eingeben, um eine digitale Mediendatei anzugeben, die abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1512e-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="1512e-118">Das Button-Element führt JScript aus, das die Datei öffnet und Windows Media Player startet.</span><span class="sxs-lookup"><span data-stu-id="1512e-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="1512e-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1512e-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="1512e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1512e-120">Requirements</span></span>



| <span data-ttu-id="1512e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1512e-121">Requirement</span></span> | <span data-ttu-id="1512e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1512e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1512e-123">Version</span><span class="sxs-lookup"><span data-stu-id="1512e-123">Version</span></span><br/> | <span data-ttu-id="1512e-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1512e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1512e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1512e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1512e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1512e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1512e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1512e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1512e-128">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1512e-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





