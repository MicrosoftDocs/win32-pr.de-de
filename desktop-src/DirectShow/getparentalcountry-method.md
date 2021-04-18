---
description: Die dvdadm. getsamentalcountry-Methode ruft das Eltern Land/die Region ab, das zuletzt in der Registrierung gespeichert wurde.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Getcentalcountry-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365560"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="1577a-103">Getsamentalcountry-Methode</span><span class="sxs-lookup"><span data-stu-id="1577a-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="1577a-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1577a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1577a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1577a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1577a-106">Die `DVDAdm.GetParentalCountry` -Methode ruft das Eltern Land/die Region ab, das zuletzt in der Registrierung gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="1577a-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="1577a-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1577a-107">Return Value</span></span>

<span data-ttu-id="1577a-108">Gibt eine ganze Zahl zurück, die den in der Registrierung gespeicherten Standard Code für Land/Region angibt.</span><span class="sxs-lookup"><span data-stu-id="1577a-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="1577a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1577a-109">Remarks</span></span>

<span data-ttu-id="1577a-110">Das Land bzw. die Region, das von dieser Methode abgerufen wird, ist nicht notwendigerweise dasselbe Land/eine Region, das zurzeit im mswebdvd-Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1577a-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1577a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1577a-111">Requirements</span></span>



| <span data-ttu-id="1577a-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1577a-112">Requirement</span></span> | <span data-ttu-id="1577a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1577a-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1577a-114">Header</span><span class="sxs-lookup"><span data-stu-id="1577a-114">Header</span></span><br/> | <dl> <span data-ttu-id="1577a-115"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="1577a-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1577a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1577a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1577a-117">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="1577a-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




