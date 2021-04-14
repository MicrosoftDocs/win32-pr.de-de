---
description: Die dvdadm. defaultsubpicturelcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für den subbildstream fest oder ruft Sie ab.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Defaultsubpicturelcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522784"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="14941-103">Defaultsubpicturelcid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="14941-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="14941-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14941-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="14941-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="14941-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="14941-106">Die `DVDAdm.DefaultSubpictureLCID` -Eigenschaft legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den subbildstream fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="14941-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="14941-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14941-107">Return Value</span></span>

<span data-ttu-id="14941-108">Gibt einen ganzzahligen Wert zurück, der die vom Benutzer angegebene Standard Teilbild-LCID darstellt, wie in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14941-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="14941-109">Dieser Wert ist nicht notwendigerweise identisch mit dem standardsubbildstream, wie er auf der DVD erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="14941-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="14941-110">Informationen zum Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="14941-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="14941-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14941-111">Remarks</span></span>

<span data-ttu-id="14941-112">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="14941-112">This property is read/write with no default value.</span></span> <span data-ttu-id="14941-113">Wenn keine standardmäßige unter Bild-LCID angegeben ist, wird das msdvdadm-Objekt den subbildstream wiedergeben, der als Standarddaten Strom auf der Festplatte gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="14941-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="14941-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14941-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14941-115">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="14941-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



