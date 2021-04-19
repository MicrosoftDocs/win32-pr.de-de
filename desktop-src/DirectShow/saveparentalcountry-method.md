---
description: Die dvdadm. saveparameentalcountry-Methode speichert das neue Eltern Land/die Region der Anwendung in der Registrierung.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Saveparameentalcountry-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354199"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="fee16-103">Saveparameentalcountry-Methode</span><span class="sxs-lookup"><span data-stu-id="fee16-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="fee16-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fee16-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fee16-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fee16-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fee16-106">Die `DVDAdm.SaveParentalCountry` -Methode speichert das neue Eltern Land/die Region der Anwendung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fee16-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="fee16-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fee16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee16-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="fee16-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="fee16-109">Gibt das Eltern Land/die Region als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="fee16-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="fee16-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="fee16-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="fee16-111">Gibt den Benutzernamen als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fee16-111">Specifies the user name as a String.</span></span> <span data-ttu-id="fee16-112">(Wird zurzeit ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="fee16-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="fee16-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="fee16-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="fee16-114">Gibt das Kennwort als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fee16-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee16-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fee16-115">Return value</span></span>

<span data-ttu-id="fee16-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fee16-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee16-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fee16-117">Remarks</span></span>

<span data-ttu-id="fee16-118">Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung für das elterliche Land/die Region in der Registrierung speichern.</span><span class="sxs-lookup"><span data-stu-id="fee16-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="fee16-119">Wie bei allen Methoden von **msdvdadm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. Es wird nur die Registrierungs Einstellung geändert, sodass das nächste Mal, wenn das mswebdvd-Objekt erstellt wird, mit dem neuen Land/der neuen Region geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fee16-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="fee16-120">Um das Eltern Land/die Region im Player zu ändern, müssen Sie [**selectpartalcountry**](selectparentalcountry-method.md)anrufen, wodurch die Registrierungs Einstellung nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fee16-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee16-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fee16-121">Requirements</span></span>



| <span data-ttu-id="fee16-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fee16-122">Requirement</span></span> | <span data-ttu-id="fee16-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fee16-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fee16-124">Header</span><span class="sxs-lookup"><span data-stu-id="fee16-124">Header</span></span><br/> | <dl> <span data-ttu-id="fee16-125"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee16-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee16-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fee16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee16-127">**Saveparameentallevel**</span><span class="sxs-lookup"><span data-stu-id="fee16-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="fee16-128">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="fee16-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




