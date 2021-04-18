---
description: Die selectparser-allevel-Methode legt die angegebene Jugend Stufe für die nachfolgende Wiedergabe fest.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Selectparser-allevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521272"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="37a23-103">Selectparser-allevel-Methode</span><span class="sxs-lookup"><span data-stu-id="37a23-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="37a23-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37a23-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="37a23-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="37a23-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="37a23-106">Die- `SelectParentalLevel` Methode legt die angegebene Jugend Stufe für die nachfolgende Wiedergabe fest.</span><span class="sxs-lookup"><span data-stu-id="37a23-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="37a23-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="37a23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a23-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="37a23-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="37a23-109">Gibt die Jugend Verwaltungsebene als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="37a23-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="37a23-110">Um die Eltern Verwaltung zu aktivieren, muss der *iLevel* -Parameter zwischen 1 und 8 liegen.</span><span class="sxs-lookup"><span data-stu-id="37a23-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="37a23-111">Um die Jugendverwaltung zu deaktivieren, legen Sie *iLevel* auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="37a23-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="37a23-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="37a23-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="37a23-113">Gibt den aktuellen Benutzer als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="37a23-113">Specifies the current user as a String.</span></span> <span data-ttu-id="37a23-114">(Wird zurzeit ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="37a23-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="37a23-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="37a23-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="37a23-116">Gibt das Kennwort an, das zurzeit als Zeichenfolge in der Registrierung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="37a23-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a23-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37a23-117">Return Value</span></span>

<span data-ttu-id="37a23-118">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="37a23-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a23-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37a23-119">Remarks</span></span>

<span data-ttu-id="37a23-120">Diese Methode legt die Zugriffsebene im mswebdvd-Objekt fest, das bestimmt, welche Inhalte der Benutzer wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="37a23-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="37a23-121">Eine höhere Ebene kann Inhalte auf niedrigerer Ebene wiedergeben, aber niedrigere Ebenen können keine Inhalte höherer Ebene wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="37a23-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="37a23-122">Die genaue Bedeutung der acht Verwaltungsebenen für die DVD ist abhängig vom Land/der Region.</span><span class="sxs-lookup"><span data-stu-id="37a23-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="37a23-123">In den USA und Kanada werden die Ebenen der Kategorie Motion Image Association of America (MPa) Rating zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="37a23-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="37a23-124">Die Eltern Verwaltung im DVD-Navigator ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="37a23-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="37a23-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37a23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a23-126">**Selectpartalcountry**</span><span class="sxs-lookup"><span data-stu-id="37a23-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="37a23-127">**Notifyparametriallevelchange**</span><span class="sxs-lookup"><span data-stu-id="37a23-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="37a23-128">**Gettitleparamevels**</span><span class="sxs-lookup"><span data-stu-id="37a23-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="37a23-129">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="37a23-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="37a23-130">**Getplayerparser**</span><span class="sxs-lookup"><span data-stu-id="37a23-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="37a23-131">**Accept-Parser-allevelchange**</span><span class="sxs-lookup"><span data-stu-id="37a23-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



