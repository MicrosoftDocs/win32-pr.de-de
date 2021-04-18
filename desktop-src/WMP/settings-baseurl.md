---
title: Settings. baseurl
description: Die baseurl-Eigenschaft gibt die Basis-URL für die relative Pfad Auflösung mit URL-Skript Befehlen an, die in Medienelemente eingebettet sind, oder ruft Sie ab.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- "\"Settings. BaseURL\"-Windows-Media Player"
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368305"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="648b9-104">Settings. baseurl</span><span class="sxs-lookup"><span data-stu-id="648b9-104">Settings.baseURL</span></span>

<span data-ttu-id="648b9-105">Die **baseurl** -Eigenschaft gibt die Basis-URL für die relative Pfad Auflösung mit URL-Skript Befehlen an, die in Medienelemente eingebettet sind, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="648b9-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="648b9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="648b9-106">Syntax</span></span>

<span data-ttu-id="648b9-107">Player. Settings. baseurl</span><span class="sxs-lookup"><span data-stu-id="648b9-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="648b9-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="648b9-108">Possible Values</span></span>

<span data-ttu-id="648b9-109">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="648b9-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="648b9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="648b9-110">Remarks</span></span>

<span data-ttu-id="648b9-111">Diese Eigenschaft gibt die Basis-http-URL an, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="648b9-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="648b9-112">Die Basis-URL wird wie folgt mit der relative URL verkettet:</span><span class="sxs-lookup"><span data-stu-id="648b9-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="648b9-113">Ein nach gestellter Schrägstrich (/) wird dem Wert der **baseurl** -Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="648b9-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="648b9-114">Ein führender Zeitraum, ein umgekehrter Schrägstrich oder ein Schrägstrich (., \\ , und/) werden aus dem relative URL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="648b9-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="648b9-115">Der relative URL wird am Ende der Basis-URL hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="648b9-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="648b9-116">Alle Schrägstriche in der resultierenden voll qualifizierten URL werden in der gleichen Richtung (konvertiert in vorwärts-oder rückwärts Schrägstriche) basierend auf der Richtung des ersten Schrägstrichs in der neuen URL gezeigt.</span><span class="sxs-lookup"><span data-stu-id="648b9-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="648b9-117">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="648b9-117">**Note**</span></span>

<span data-ttu-id="648b9-118">Das Player-Steuerelement unterstützt nicht die Verwendung von zwei Punkten (..) im relative URL, um das übergeordnete Element des aktuellen Speicher Orts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="648b9-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="648b9-119">**Windows Media Player 10 Mobile**: Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="648b9-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="648b9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="648b9-120">Requirements</span></span>



| <span data-ttu-id="648b9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="648b9-121">Requirement</span></span> | <span data-ttu-id="648b9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="648b9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="648b9-123">Version</span><span class="sxs-lookup"><span data-stu-id="648b9-123">Version</span></span><br/> | <span data-ttu-id="648b9-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="648b9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="648b9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="648b9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="648b9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="648b9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="648b9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="648b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648b9-128">**Player. ScriptCommand-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="648b9-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="648b9-129">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="648b9-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





