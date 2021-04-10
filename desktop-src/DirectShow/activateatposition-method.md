---
description: Die activateatposition-Methode aktiviert die Menü Schaltfläche an der angegebenen Position.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Activateatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125329"
---
# <a name="activateatposition-method"></a><span data-ttu-id="2219d-103">Activateatposition-Methode</span><span class="sxs-lookup"><span data-stu-id="2219d-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="2219d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2219d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2219d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2219d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2219d-106">Die activateatposition-Methode aktiviert die Menü Schaltfläche an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="2219d-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="2219d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2219d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2219d-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*</span><span class="sxs-lookup"><span data-stu-id="2219d-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="2219d-109">Gibt die x-Koordinate als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="2219d-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="2219d-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*</span><span class="sxs-lookup"><span data-stu-id="2219d-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="2219d-111">Gibt die y-Koordinate als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="2219d-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2219d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2219d-112">Return Value</span></span>

<span data-ttu-id="2219d-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2219d-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2219d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2219d-114">Remarks</span></span>

<span data-ttu-id="2219d-115">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2219d-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2219d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2219d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2219d-117">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="2219d-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="2219d-118">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="2219d-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="2219d-119">**Getbuttonatposition**</span><span class="sxs-lookup"><span data-stu-id="2219d-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="2219d-120">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="2219d-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="2219d-121">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="2219d-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="2219d-122">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="2219d-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



