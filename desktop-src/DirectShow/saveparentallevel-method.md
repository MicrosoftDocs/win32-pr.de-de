---
description: Die dvdadm. saveparameentallevel-Methode speichert eine neue Standard-Jugend Stufe in der Registrierung.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Saveparameentallevel-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373778"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="94975-103">Saveparameentallevel-Methode</span><span class="sxs-lookup"><span data-stu-id="94975-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="94975-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94975-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="94975-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="94975-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="94975-106">Die **dvdadm. saveparameentallevel** -Methode speichert eine neue Standard-Jugend Stufe in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="94975-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="94975-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="94975-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94975-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="94975-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="94975-109">Gibt die Jugend Stufe als einen ganzzahligen Wert zwischen 1 und 8 an.</span><span class="sxs-lookup"><span data-stu-id="94975-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="94975-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="94975-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="94975-111">Gibt den Benutzernamen als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="94975-111">Specifies the user name as a String.</span></span> <span data-ttu-id="94975-112">(Wird zurzeit ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="94975-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="94975-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="94975-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="94975-114">Gibt das Kennwort als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="94975-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94975-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94975-115">Return Value</span></span>

<span data-ttu-id="94975-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="94975-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94975-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94975-117">Remarks</span></span>

<span data-ttu-id="94975-118">Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung auf Jugendebene in der Registrierung speichern.</span><span class="sxs-lookup"><span data-stu-id="94975-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="94975-119">Wie bei allen Methoden von **msdvdadm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. Es wird nur die Registrierungs Einstellung geändert, sodass das nächste Mal, wenn das mswebdvd-Objekt gestartet wird, mit der neuen Ebene geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="94975-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="94975-120">Geben Sie-1 an, um die Eltern Verwaltung zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="94975-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="94975-121">Um die Jugendebene im Player zu ändern, müssen Sie [**selectparamevel**](selectparentallevel-method.md)aufzurufen, wodurch die Registrierungs Einstellung nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="94975-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="94975-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94975-122">Requirements</span></span>



| <span data-ttu-id="94975-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94975-123">Requirement</span></span> | <span data-ttu-id="94975-124">Wert</span><span class="sxs-lookup"><span data-stu-id="94975-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94975-125">Header</span><span class="sxs-lookup"><span data-stu-id="94975-125">Header</span></span><br/> | <dl> <span data-ttu-id="94975-126"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="94975-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94975-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94975-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94975-128">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="94975-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




