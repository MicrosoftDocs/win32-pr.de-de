---
description: Die selectandactivatebutton-Methode wählt die angegebene Schaltfläche aus und aktiviert Sie.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Selectandactivatebutton-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346187"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="87778-103">Selectandactivatebutton-Methode</span><span class="sxs-lookup"><span data-stu-id="87778-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="87778-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="87778-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="87778-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="87778-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="87778-106">Die `SelectAndActivateButton` -Methode wählt die angegebene Schaltfläche aus und aktiviert Sie.</span><span class="sxs-lookup"><span data-stu-id="87778-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="87778-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87778-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87778-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="87778-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="87778-109">Gibt die Schaltfläche als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="87778-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87778-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87778-110">Return Value</span></span>

<span data-ttu-id="87778-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="87778-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87778-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87778-112">Remarks</span></span>

<span data-ttu-id="87778-113">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="87778-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="87778-114">Mit dieser Methode wird die angegebene Schaltfläche hervorgehoben und automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="87778-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="87778-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87778-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87778-116">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="87778-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="87778-117">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="87778-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="87778-118">**Activatebutton**</span><span class="sxs-lookup"><span data-stu-id="87778-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="87778-119">**Getbuttonatposition**</span><span class="sxs-lookup"><span data-stu-id="87778-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="87778-120">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="87778-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="87778-121">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="87778-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



