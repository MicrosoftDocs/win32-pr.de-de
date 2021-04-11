---
description: "\"Getplayerparameentallevel\" Ruft die im mswebdvd-Objekt festgelegte Jugend Verwaltungsebene ab."
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Getplayerparameentallevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123499"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="d9648-103">Getplayerparameentallevel-Methode</span><span class="sxs-lookup"><span data-stu-id="d9648-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="d9648-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9648-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d9648-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d9648-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d9648-106">Der `GetPlayerParentalLevel` Ruft die im **mswebdvd** -Objekt festgelegte Jugend Verwaltungsebene ab.</span><span class="sxs-lookup"><span data-stu-id="d9648-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="d9648-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9648-107">Return Value</span></span>

<span data-ttu-id="d9648-108">Gibt einen ganzzahligen Wert zurück, der die aktuelle Jugend Stufe im DVD-Navigator angibt, oder-1, wenn die Eltern Verwaltung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d9648-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9648-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9648-109">Remarks</span></span>

<span data-ttu-id="d9648-110">Eine Player Anwendung ist für die Erzwingung von Eltern Steuerelementen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d9648-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="d9648-111">Die Jugend Stufe des Players ist ein von einer Anwendung fest gelegteter Wert, der verwendet werden kann, um die höchste Jugend Stufe anzugeben, die der aktuelle Benutzer anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="d9648-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="d9648-112">Wenn der DVD-Navigator auf eine neue Jugend Stufe trifft, verwenden Sie diese Methode, um zu bestimmen, ob die neue Ebene größer ist als die Ebene, die von der Anwendung über [**selectparameentallevel**](selectparentallevel-method.md)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9648-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9648-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9648-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9648-114">**Gettitleparamevels**</span><span class="sxs-lookup"><span data-stu-id="d9648-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="d9648-115">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="d9648-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="d9648-116">**Selectpartalcountry**</span><span class="sxs-lookup"><span data-stu-id="d9648-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="d9648-117">**Selectparser-allevel**</span><span class="sxs-lookup"><span data-stu-id="d9648-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



