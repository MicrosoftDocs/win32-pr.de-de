---
title: Network. BufferingTime
description: Die BufferingTime-Eigenschaft gibt den Zeitraum in Millisekunden an, der für die Pufferung eingehender Daten reserviert ist, bevor die Wiedergabe beginnt.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network. BufferingTime-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369604"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="45a6f-104">Network. BufferingTime</span><span class="sxs-lookup"><span data-stu-id="45a6f-104">Network.bufferingTime</span></span>

<span data-ttu-id="45a6f-105">Die **BufferingTime** -Eigenschaft gibt den Zeitraum in Millisekunden an, der für die Pufferung eingehender Daten reserviert ist, bevor die Wiedergabe beginnt.</span><span class="sxs-lookup"><span data-stu-id="45a6f-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a6f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="45a6f-106">Syntax</span></span>

<span data-ttu-id="45a6f-107">*Player*. *Netzwerk*. **BufferingTime**</span><span class="sxs-lookup"><span data-stu-id="45a6f-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="45a6f-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="45a6f-108">Possible Values</span></span>

<span data-ttu-id="45a6f-109">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) im Bereich von 0 (null) bis 60.000 mit dem Standardwert 5.000. </span><span class="sxs-lookup"><span data-stu-id="45a6f-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="45a6f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45a6f-110">Examples</span></span>

<span data-ttu-id="45a6f-111">Im folgenden JScript-Beispiel wird *Network* verwendet. **BufferingTime** zum Angeben der Anzahl von Sekunden, die für die Pufferung eingehender Daten reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="45a6f-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="45a6f-112">Die Informationen werden aus einem HTML-Text Eingabe Element abgerufen, das mit ID = "buftext" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="45a6f-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="45a6f-113">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="45a6f-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="45a6f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45a6f-114">Requirements</span></span>



| <span data-ttu-id="45a6f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45a6f-115">Requirement</span></span> | <span data-ttu-id="45a6f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="45a6f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45a6f-117">Version</span><span class="sxs-lookup"><span data-stu-id="45a6f-117">Version</span></span><br/> | <span data-ttu-id="45a6f-118">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="45a6f-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="45a6f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="45a6f-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="45a6f-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45a6f-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45a6f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45a6f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a6f-122">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="45a6f-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





