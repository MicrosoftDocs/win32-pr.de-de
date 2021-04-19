---
description: Die dvdadm. defaultaudiolcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für den Audiostream fest oder ruft Sie ab.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Defaultaudiolcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346412"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="9c584-103">Defaultaudiolcid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c584-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="9c584-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c584-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c584-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9c584-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c584-106">Die `DVDAdm.DefaultAudioLCID` -Eigenschaft legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="9c584-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="9c584-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c584-107">Return Value</span></span>

<span data-ttu-id="9c584-108">Gibt einen ganzzahligen Wert zurück, der die vom Benutzer angegebene standardaudiolcid darstellt, die in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9c584-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="9c584-109">Dieser Wert ist nicht notwendigerweise identisch mit dem Standardaudiostream, wie er auf der DVD erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c584-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c584-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c584-110">Remarks</span></span>

<span data-ttu-id="9c584-111">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9c584-111">This property is read/write with no default value.</span></span> <span data-ttu-id="9c584-112">Wenn keine standardaudiolcid angegeben ist, wird das msdvdadm-Objekt den Audiostream wiedergeben, der als Standarddaten Strom auf der Festplatte gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="9c584-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c584-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c584-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c584-114">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="9c584-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



