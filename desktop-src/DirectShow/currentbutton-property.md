---
description: Die currentbutton-Eigenschaft ruft die Nummer der ausgewählten Menü Schaltfläche ab.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Currentbutton (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341859"
---
# <a name="currentbutton-property"></a><span data-ttu-id="19cd0-103">Currentbutton (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="19cd0-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="19cd0-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19cd0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="19cd0-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="19cd0-106">Die- `CurrentButton` Eigenschaft ruft die Nummer der ausgewählten Menü Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="19cd0-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="19cd0-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19cd0-107">Return Value</span></span>

<span data-ttu-id="19cd0-108">Gibt eine Ganzzahl zurück, die die Schaltfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="19cd0-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="19cd0-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19cd0-109">Remarks</span></span>

<span data-ttu-id="19cd0-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="19cd0-110">This property is read-only with no default value.</span></span> <span data-ttu-id="19cd0-111">Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="19cd0-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="19cd0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19cd0-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cd0-113">**Activatebutton**</span><span class="sxs-lookup"><span data-stu-id="19cd0-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="19cd0-114">**Buttonsavailable**</span><span class="sxs-lookup"><span data-stu-id="19cd0-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="19cd0-115">**Getbuttonatposition**</span><span class="sxs-lookup"><span data-stu-id="19cd0-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="19cd0-116">**Getbuttonrect**</span><span class="sxs-lookup"><span data-stu-id="19cd0-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="19cd0-117">**Selectandactivatebutton**</span><span class="sxs-lookup"><span data-stu-id="19cd0-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="19cd0-118">**Selectatposition**</span><span class="sxs-lookup"><span data-stu-id="19cd0-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



