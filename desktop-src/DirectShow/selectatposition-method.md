---
description: Die selectatposition-Methode wählt die Menü Schaltfläche an den angegebenen Koordinaten des Mauszeigers aus.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Selectatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746249"
---
# <a name="selectatposition-method"></a><span data-ttu-id="8a32f-103">Selectatposition-Methode</span><span class="sxs-lookup"><span data-stu-id="8a32f-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="8a32f-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a32f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8a32f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8a32f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8a32f-106">Die- `SelectAtPosition` Methode wählt die Menü Schaltfläche an den angegebenen Koordinaten des Mauszeigers aus.</span><span class="sxs-lookup"><span data-stu-id="8a32f-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="8a32f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a32f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a32f-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*</span><span class="sxs-lookup"><span data-stu-id="8a32f-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="8a32f-109">Gibt die x-Koordinate als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="8a32f-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8a32f-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*</span><span class="sxs-lookup"><span data-stu-id="8a32f-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="8a32f-111">Gibt die y-Koordinate als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="8a32f-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a32f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a32f-112">Return Value</span></span>

<span data-ttu-id="8a32f-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8a32f-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a32f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a32f-114">Remarks</span></span>

<span data-ttu-id="8a32f-115">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="8a32f-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="8a32f-116">Durch Auswahl von wird nur die Schaltfläche hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="8a32f-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="8a32f-117">Um den Befehl zu senden, der einer ausgewählten Schaltfläche zugeordnet ist, aufrufen Sie [**activatebutton**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="8a32f-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a32f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a32f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a32f-119">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="8a32f-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="8a32f-120">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="8a32f-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="8a32f-121">**Getbuttonatposition**</span><span class="sxs-lookup"><span data-stu-id="8a32f-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="8a32f-122">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="8a32f-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="8a32f-123">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="8a32f-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



