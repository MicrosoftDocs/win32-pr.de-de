---
description: Die dvdadm. bookmarkonstoppt-Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der dem mswebdvd-Objekt mitteilt, ob ein Lesezeichen des aktuellen Speicher Orts und der Einstellungen automatisch gespeichert werden soll, wenn der Benutzer auf die Schaltfläche Beenden klickt.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Bookmarkonstoppt (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125054"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="cfdbb-103">Bookmarkonstoppt (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cfdbb-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="cfdbb-104">Die- `DVDAdm.BookmarkOnStop` Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der das mswebdvd-Objekt anweist, ob ein Lesezeichen des aktuellen Speicher Orts und **der** Einstellungen automatisch gespeichert werden soll, wenn der Benutzer auf die Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="cfdbb-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="cfdbb-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfdbb-105">Return Value</span></span>

<span data-ttu-id="cfdbb-106">Gibt einen booleschen Wert zurück, der angibt, ob das msdvdadm-Objekt ein Lesezeichen aller DVD-Einstellungen speichert, einschließlich der Position auf der Festplatte, der Jugendebene und dem Eltern Land/der Region</span><span class="sxs-lookup"><span data-stu-id="cfdbb-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfdbb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfdbb-107">Remarks</span></span>

<span data-ttu-id="cfdbb-108">Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="cfdbb-109">Lesezeichen sind nur für einen bestimmten Computer gültig.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="cfdbb-110">Ein Benutzer kann ein Lesezeichen nicht speichern und dann an eine andere Person senden, um Sie auf einem anderen Computer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfdbb-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfdbb-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdbb-112">**Bookmarkonclose**</span><span class="sxs-lookup"><span data-stu-id="cfdbb-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="cfdbb-113">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="cfdbb-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



