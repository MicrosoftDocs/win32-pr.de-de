---
description: Die getgprm-Methode ruft das angegebene allgemeine Parameter Register ab.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Getgprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522312"
---
# <a name="getgprm-method"></a><span data-ttu-id="b253b-103">Getgprm-Methode</span><span class="sxs-lookup"><span data-stu-id="b253b-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="b253b-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b253b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b253b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b253b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b253b-106">Die- `GetGPRM` Methode ruft das angegebene allgemeine Parameter Register ab.</span><span class="sxs-lookup"><span data-stu-id="b253b-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="b253b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b253b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b253b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="b253b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="b253b-109">Gibt das Register an, das als ganze Zahl abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b253b-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="b253b-110">Der Wert muss zwischen 0 und 15 liegen.</span><span class="sxs-lookup"><span data-stu-id="b253b-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b253b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b253b-111">Return Value</span></span>

<span data-ttu-id="b253b-112">Gibt einen ganzzahligen Wert zurück, der das angegebene Register darstellt.</span><span class="sxs-lookup"><span data-stu-id="b253b-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b253b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b253b-113">Remarks</span></span>

<span data-ttu-id="b253b-114">Diese Methode ist für DVD-Navigations-oder Wiedergabe Funktionen mit dem **mswebdvd** -Objekt nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b253b-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="b253b-115">Sie wird für diejenigen bereitgestellt, die über ein umfassendes Verständnis der DVD-Spezifikation verfügen, die erweiterte Funktionen implementieren möchte.</span><span class="sxs-lookup"><span data-stu-id="b253b-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="b253b-116">Gprms können verwendet werden, um beliebige Werte zu speichern, sodass Sie frei festgelegt und gelesen werden können.</span><span class="sxs-lookup"><span data-stu-id="b253b-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="b253b-117">Da jedoch gprms auch zum Speichern von Disk-Befehlen verwendet werden, kann das Ändern ihrer Werte mithilfe von [**setgprm**](setgprm-method.md) zu unvorhersehbarem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="b253b-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="b253b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b253b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b253b-119">**Setgprm**</span><span class="sxs-lookup"><span data-stu-id="b253b-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



