---
description: Die dvdadm. getparameentallevel-Methode ruft die Jugend Stufe ab, die zuletzt in der Registrierung gespeichert wurde.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Getparameentallevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392365"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="cd697-103">Getparameentallevel-Methode</span><span class="sxs-lookup"><span data-stu-id="cd697-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="cd697-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd697-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cd697-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cd697-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cd697-106">Die- `DVDAdm.GetParentalLevel` Methode ruft die Jugend Stufe ab, die zuletzt in der Registrierung gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd697-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="cd697-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd697-107">Return Value</span></span>

<span data-ttu-id="cd697-108">Gibt eine ganze Zahl zwischen 1 und 8 zurück, die die standardmäßige Jugend Stufe angibt.</span><span class="sxs-lookup"><span data-stu-id="cd697-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd697-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd697-109">Remarks</span></span>

<span data-ttu-id="cd697-110">Die von dieser Methode abgerufenen elternebene ist nicht notwendigerweise die gleiche Ebene, die derzeit im mswebdvd-Steuerelement gespeichert ist. um die derzeit im-Steuerelement gespeicherte Ebene abzurufen, nennen Sie die [**getplayerparameentallevel**](getplayerparentallevel-method.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cd697-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="cd697-111">Der Wert-1 gibt an, dass die Eltern Verwaltung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cd697-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd697-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd697-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd697-113">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="cd697-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



