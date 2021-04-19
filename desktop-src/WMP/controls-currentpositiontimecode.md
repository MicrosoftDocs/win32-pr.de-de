---
title: Controls. currentPositionTimecode
description: Die currentPositionTimecode-Eigenschaft gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Steuerelemente. currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356332"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="8ca0c-105">Controls. currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="8ca0c-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="8ca0c-106">Die **currentPositionTimecode** -Eigenschaft gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="8ca0c-107">Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="8ca0c-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="8ca0c-108">Possible Values</span></span>

<span data-ttu-id="8ca0c-109">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca0c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ca0c-110">Remarks</span></span>

<span data-ttu-id="8ca0c-111">Der SMPTE-Zeit Code stellt eine Standardmethode zum Identifizieren eines einzelnen Video Rahmens dar, der für die Synchronisierung der Wiedergabe nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="8ca0c-112">Wenn eine digitale Mediendatei SMPTE-Zeit Code unterstützt, können Windows-Media Player die aktuellen Zeit Code Positionsinformationen abrufen oder einen Video Frame suchen, der durch eine bestimmte Zeit Code **Zeichenfolge** identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="8ca0c-113">Der SMPTE-Zeit Code identifiziert einen bestimmten Frame um die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Verweis Rahmen aus dem Frame trennen, der als Zeit NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="8ca0c-114">Normalerweise ist der Zeit Null-Frame der Anfang der Datei, und ein bestimmter SMPTE-Zeit Codewert stellt die verstrichene Zeit seit dem Start der Datei dar.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="8ca0c-115">Die Zeit Code **Zeichenfolge** liegt im Format \[ *Bereich* \] *HH*:*mm*:*SS*.*FF* , wobei \[ *Range* \] den Bereich darstellt, *HH* stellt Stunden, *mm* stellt Minuten dar, *SS* stellt Sekunden dar, und *FF* stellt Frames dar.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="8ca0c-116">Wenn Sie mithilfe von **currentPositionTimecode** einen Wert angeben, müssen Sie alle acht Ziffern mit Nullen als Platzhalter einschließen.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="8ca0c-117">Der \[  \] Bereichsspezifizierer entspricht dem **Wrange** -Member der **WMT- \_ \_ Erweiterungs \_ Daten** Struktur von Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="8ca0c-118">Weitere Informationen zu Zeit Codebereichen finden Sie im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="8ca0c-119">Das angeben und Abrufen von **currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeit Code Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="8ca0c-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ca0c-120">Examples</span></span>

<span data-ttu-id="8ca0c-121">Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, 0 Minuten, 30 Sekunden und 5 Frames angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="8ca0c-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="8ca0c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ca0c-123">Requirements</span></span>



| <span data-ttu-id="8ca0c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ca0c-124">Requirement</span></span> | <span data-ttu-id="8ca0c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8ca0c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0c-126">Version</span><span class="sxs-lookup"><span data-stu-id="8ca0c-126">Version</span></span><br/> | <span data-ttu-id="8ca0c-127">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="8ca0c-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="8ca0c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca0c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ca0c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca0c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca0c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ca0c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca0c-131">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="8ca0c-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





