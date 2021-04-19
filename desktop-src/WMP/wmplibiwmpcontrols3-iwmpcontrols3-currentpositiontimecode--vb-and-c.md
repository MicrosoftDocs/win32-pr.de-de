---
title: IWMPControls3 currentPositionTimecode (Eigenschaft)
description: Die currentPositionTimecode-Eigenschaft ruft die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats ab oder legt diese fest. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- currentPositionTimecode-Eigenschaften Fenster Media Player
- currentPositionTimecode-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentPositionTimecode-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365778"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="22d39-107">IWMPControls3:: currentPositionTimecode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22d39-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="22d39-108">Die **currentPositionTimecode** -Eigenschaft ruft die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="22d39-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="22d39-109">Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="22d39-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d39-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d39-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="22d39-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="22d39-111">Property value</span></span>

<span data-ttu-id="22d39-112">Eine **System. String** , bei der es sich um den SMPTE-Zeit Code handelt.</span><span class="sxs-lookup"><span data-stu-id="22d39-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d39-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22d39-113">Remarks</span></span>

<span data-ttu-id="22d39-114">Der SMPTE-Zeit Code stellt eine Standardmethode zum Identifizieren eines einzelnen Video Rahmens dar, der für die Synchronisierung der Wiedergabe nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="22d39-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="22d39-115">Wenn eine digitale Mediendatei SMPTE-Zeit Code unterstützt, können Windows Media Player die aktuellen Zeit Code Positionsinformationen abrufen oder einen Video Frame suchen, der durch einen bestimmten Zeit Code gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="22d39-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="22d39-116">Der SMPTE-Zeit Code identifiziert einen bestimmten Frame um die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Verweis Rahmen aus dem Frame trennen, der als Zeit NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22d39-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="22d39-117">Normalerweise ist der Zeit Null-Frame der Anfang der Datei, und ein bestimmter SMPTE-Zeit Codewert stellt die verstrichene Zeit seit dem Start der Datei dar.</span><span class="sxs-lookup"><span data-stu-id="22d39-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="22d39-118">Der Zeit Code liegt im Format \[ *Bereich* \] *HH*:*mm*:*SS*.*FF* , wobei \[ *Range* \] den Bereich darstellt, hh stellt Stunden, *mm* stellt Minuten dar, *SS* stellt Sekunden dar, und *FF* stellt Frames dar.</span><span class="sxs-lookup"><span data-stu-id="22d39-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="22d39-119">Wenn Sie einen Wert für **currentPositionTimecode** festlegen, müssen Sie alle acht Ziffern einschließen, wobei Sie Nullen als Platzhalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="22d39-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="22d39-120">\[*Bereich* \] entspricht dem **Wrange** -Member der **WMT- \_ \_ Erweiterungs \_ Daten** Struktur "Windows Media-Format".</span><span class="sxs-lookup"><span data-stu-id="22d39-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="22d39-121">Weitere Informationen zu Zeit Codebereichen finden Sie im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="22d39-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="22d39-122">Das Festlegen und das erhalten von **currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeit Code Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="22d39-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="22d39-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22d39-123">Examples</span></span>

<span data-ttu-id="22d39-124">Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, 0 Minuten, 30 Sekunden und 5 Frames angegeben.</span><span class="sxs-lookup"><span data-stu-id="22d39-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="22d39-125">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="22d39-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="22d39-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22d39-126">Requirements</span></span>



| <span data-ttu-id="22d39-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22d39-127">Requirement</span></span> | <span data-ttu-id="22d39-128">Wert</span><span class="sxs-lookup"><span data-stu-id="22d39-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d39-129">Version</span><span class="sxs-lookup"><span data-stu-id="22d39-129">Version</span></span><br/>   | <span data-ttu-id="22d39-130">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="22d39-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="22d39-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="22d39-131">Namespace</span></span><br/> | <span data-ttu-id="22d39-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="22d39-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="22d39-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="22d39-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="22d39-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="22d39-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d39-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22d39-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d39-136">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="22d39-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





