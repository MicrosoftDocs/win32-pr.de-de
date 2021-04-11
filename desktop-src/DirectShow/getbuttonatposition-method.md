---
description: Die getbuttonatposition-Methode ruft die Nummer der Schaltfläche an den angegebenen Koordinaten ab, ohne sie auszuwählen oder zu aktivieren.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Getbuttonatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123536"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="98fec-103">Getbuttonatposition-Methode</span><span class="sxs-lookup"><span data-stu-id="98fec-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="98fec-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98fec-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="98fec-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="98fec-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="98fec-106">Die- `GetButtonAtPosition` Methode ruft die Nummer der Schaltfläche an den angegebenen Koordinaten ab, ohne sie auszuwählen oder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="98fec-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="98fec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98fec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fec-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*</span><span class="sxs-lookup"><span data-stu-id="98fec-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="98fec-109">Gibt die x-Koordinate des Mauszeigers als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="98fec-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="98fec-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*</span><span class="sxs-lookup"><span data-stu-id="98fec-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="98fec-111">Gibt die y-Koordinate des Mauszeigers als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="98fec-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fec-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98fec-112">Return Value</span></span>

<span data-ttu-id="98fec-113">Gibt einen ganzzahligen Wert zurück, der die Schaltfläche an der angegebenen Position angibt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98fec-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="98fec-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98fec-114">Remarks</span></span>

<span data-ttu-id="98fec-115">Diese Methode gibt 0 (null) zurück, wenn keine Schaltfläche an den angegebenen Koordinaten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="98fec-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="98fec-116">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="98fec-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="98fec-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98fec-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fec-118">**Activatebutton**</span><span class="sxs-lookup"><span data-stu-id="98fec-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="98fec-119">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="98fec-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="98fec-120">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="98fec-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="98fec-121">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="98fec-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="98fec-122">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="98fec-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="98fec-123">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="98fec-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



