---
description: Die selectsamentalcountry-Methode legt das angegebene jugendland/die angegebene Region für die nachfolgende Wiedergabe fest.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Selectsamentalcountry-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522179"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="78a63-103">Selectsamentalcountry-Methode</span><span class="sxs-lookup"><span data-stu-id="78a63-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="78a63-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78a63-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78a63-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="78a63-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78a63-106">Die `SelectParentalCountry` -Methode legt das angegebene Eltern Land/die angegebene Region für nachfolgende Wiedergabe fest.</span><span class="sxs-lookup"><span data-stu-id="78a63-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="78a63-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="78a63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78a63-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="78a63-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="78a63-109">Gibt das Land/die Region als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="78a63-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="78a63-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="78a63-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="78a63-111">Gibt den aktuell angemeldeten Benutzer als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="78a63-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="78a63-112">(Wird zurzeit ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="78a63-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="78a63-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="78a63-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="78a63-114">Gibt die Anwendungs Kennwort-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="78a63-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78a63-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78a63-115">Return Value</span></span>

<span data-ttu-id="78a63-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="78a63-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78a63-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78a63-117">Remarks</span></span>

<span data-ttu-id="78a63-118">Das elterliche Land/die Region bestimmt, wie die Jugend Stufen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="78a63-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="78a63-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78a63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a63-120">**Selectparser-allevel**</span><span class="sxs-lookup"><span data-stu-id="78a63-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="78a63-121">**Notifyparametriallevelchange**</span><span class="sxs-lookup"><span data-stu-id="78a63-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="78a63-122">**Gettitleparamevels**</span><span class="sxs-lookup"><span data-stu-id="78a63-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="78a63-123">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="78a63-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="78a63-124">**Getplayerparser**</span><span class="sxs-lookup"><span data-stu-id="78a63-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="78a63-125">**Accept-Parser-allevelchange**</span><span class="sxs-lookup"><span data-stu-id="78a63-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



