---
description: Die buttonsavailable-Eigenschaft ruft die Gesamtzahl der Schaltflächen im aktuellen Menü ab.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Buttonsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392750"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="f4346-103">Buttonsavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4346-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="f4346-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f4346-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f4346-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f4346-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f4346-106">Die- `ButtonsAvailable` Eigenschaft ruft die Gesamtanzahl der Schaltflächen im aktuellen Menü ab.</span><span class="sxs-lookup"><span data-stu-id="f4346-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="f4346-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4346-107">Return Value</span></span>

<span data-ttu-id="f4346-108">Gibt einen Integer-Wert zurück, der die Anzahl der Schaltflächen darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4346-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4346-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4346-109">Remarks</span></span>

<span data-ttu-id="f4346-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="f4346-110">This property is read-only with no default value.</span></span> <span data-ttu-id="f4346-111">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="f4346-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="f4346-112">Rufen Sie diese Methode auf, um die Obergrenze für den Bereich gültiger Schaltflächen Nummern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f4346-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4346-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4346-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4346-114">**Currentbutton**</span><span class="sxs-lookup"><span data-stu-id="f4346-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="f4346-115">**Getbuttonatposition**</span><span class="sxs-lookup"><span data-stu-id="f4346-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="f4346-116">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="f4346-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="f4346-117">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="f4346-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="f4346-118">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="f4346-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



