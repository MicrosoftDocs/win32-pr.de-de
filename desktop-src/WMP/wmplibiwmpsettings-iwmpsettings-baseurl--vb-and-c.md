---
title: Iwmpsettings baseurl (Eigenschaft)
description: Die baseurl-Eigenschaft ruft die Basis-URL ab oder legt Sie fest, die für die relative Pfad Auflösung mit URL-Skript Befehlen verwendet wird, die in Inhalte digitaler Medien eingebettet sind
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseurl-Eigenschaften Fenster Media Player
- baseurl-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, baseurl-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369531"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="62ce4-106">Iwmpsettings:: baseurl (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62ce4-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="62ce4-107">Die **baseurl** -Eigenschaft ruft die Basis-URL ab oder legt Sie fest, die für die relative Pfad Auflösung mit URL-Skript Befehlen verwendet wird, die in Inhalte digitaler Medien eingebettet sind</span><span class="sxs-lookup"><span data-stu-id="62ce4-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ce4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ce4-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="62ce4-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="62ce4-109">Property value</span></span>

<span data-ttu-id="62ce4-110">Ein **System. String** -Wert, der die Basis-URL ist.</span><span class="sxs-lookup"><span data-stu-id="62ce4-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="62ce4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62ce4-111">Remarks</span></span>

<span data-ttu-id="62ce4-112">Diese Eigenschaft gibt die Basis-http-URL an, die vom **AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent** -Ereignis als Befehlsparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="62ce4-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="62ce4-113">Die Basis-URL wird wie folgt mit der relative URL verkettet:</span><span class="sxs-lookup"><span data-stu-id="62ce4-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="62ce4-114">Dem Wert, der von der **baseurl** -Eigenschaft abgerufen wird, wird ein nach stehender Schrägstrich (/) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62ce4-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="62ce4-115">Ein führender Zeitraum, ein umgekehrter Schrägstrich oder ein Schrägstrich (., \\ , und/) wird aus der relative URL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="62ce4-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="62ce4-116">Der relative URL wird am Ende der Basis-URL hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62ce4-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="62ce4-117">Alle Schrägstriche in der resultierenden voll qualifizierten URL werden in der gleichen Richtung (konvertiert in vorwärts-oder rückwärts Schrägstriche) basierend auf der Richtung des ersten Schrägstrichs in der neuen URL gezeigt.</span><span class="sxs-lookup"><span data-stu-id="62ce4-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="62ce4-118">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="62ce4-118">**Note**</span></span>

<span data-ttu-id="62ce4-119">Das Windows Media Player-Steuerelement unterstützt nicht die Verwendung von zwei Punkten (..) in der relative URL, um das übergeordnete Element des aktuellen Speicher Orts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="62ce4-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ce4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62ce4-120">Requirements</span></span>



| <span data-ttu-id="62ce4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ce4-121">Requirement</span></span> | <span data-ttu-id="62ce4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="62ce4-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ce4-123">Version</span><span class="sxs-lookup"><span data-stu-id="62ce4-123">Version</span></span><br/>   | <span data-ttu-id="62ce4-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="62ce4-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="62ce4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="62ce4-125">Namespace</span></span><br/> | <span data-ttu-id="62ce4-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="62ce4-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="62ce4-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="62ce4-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62ce4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="62ce4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ce4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ce4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ce4-130">**AxWindowsMediaPlayer. ScriptCommand-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="62ce4-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="62ce4-131">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="62ce4-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





