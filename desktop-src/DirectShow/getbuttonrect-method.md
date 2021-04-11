---
description: Die getbuttonrect-Methode ruft das Rechteck für die angegebene Schaltfläche in Fenster Koordinaten ab.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Getbuttonrect-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123535"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="44366-103">Getbuttonrect-Methode</span><span class="sxs-lookup"><span data-stu-id="44366-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="44366-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44366-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="44366-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="44366-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="44366-106">Die- `GetButtonRect` Methode ruft das Rechteck für die angegebene Schaltfläche in Fenster Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="44366-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="44366-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="44366-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44366-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="44366-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="44366-109">Gibt die Schaltflächen Nummer als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="44366-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44366-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44366-110">Return Value</span></span>

<span data-ttu-id="44366-111">Gibt ein [dvdrect](dvdrect-object.md) -Objekt zurück, das das Rechteck definiert.</span><span class="sxs-lookup"><span data-stu-id="44366-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="44366-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44366-112">Remarks</span></span>

<span data-ttu-id="44366-113">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="44366-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="44366-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44366-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44366-115">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="44366-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="44366-116">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="44366-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="44366-117">**Activatebutton**</span><span class="sxs-lookup"><span data-stu-id="44366-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="44366-118">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="44366-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="44366-119">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="44366-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



