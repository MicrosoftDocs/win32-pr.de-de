---
title: QuickInfo-Stile (kommctrl. h)
description: In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelement Stile aufgelistet
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364899"
---
# <a name="tooltip-styles"></a><span data-ttu-id="69091-103">QuickInfo-Stile</span><span class="sxs-lookup"><span data-stu-id="69091-103">Tooltip Styles</span></span>

<span data-ttu-id="69091-104">In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelement Stile aufgelistet</span><span class="sxs-lookup"><span data-stu-id="69091-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="69091-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="69091-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="69091-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69091-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="69091-107"><dt>**TTS \_ alwaystip**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="69091-108">Gibt an, dass das QuickInfo-Steuerelement angezeigt wird, wenn sich der Cursor auf einem Tool befindet, auch wenn das Besitzer Fenster des QuickInfo-Steuer Elements nicht</span><span class="sxs-lookup"><span data-stu-id="69091-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="69091-109">Ohne diesen Stil wird die QuickInfo nur angezeigt, wenn das Besitzer Fenster des Tools aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="69091-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="69091-110"><dt>**TTS-Sprechblase \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="69091-111">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69091-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="69091-112">Gibt an, dass das QuickInfo-Steuerelement die Darstellung einer Zeichenfolge "Sprechblase" mit abgerundeten Ecken und einem Stamm Element anzeigt, das auf das Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="69091-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="69091-113"><dt>**TTE \_ Schließen**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="69091-114">Zeigt die Schaltfläche **Schließen** in der QuickInfo an.</span><span class="sxs-lookup"><span data-stu-id="69091-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="69091-115">Nur gültig, wenn die QuickInfo den Stil der TTS-Sprechblase \_ und einen Titel hat. siehe [**TTM \_ SetTitle**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="69091-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="69091-116"><dt>**TTS \_ noanimieren**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="69091-117">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69091-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="69091-118">Deaktiviert die Animation mit verschiebbaren QuickInfo auf Windows 98-und Windows 2000-Systemen.</span><span class="sxs-lookup"><span data-stu-id="69091-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="69091-119">Dieser Stil wird in früheren Systemen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="69091-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="69091-120"><dt>**TTS- \_ nofade**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="69091-121">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69091-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="69091-122">Deaktiviert die Animation der Ausblend-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="69091-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="69091-123"><dt>**TTS \_ NoPrefix**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="69091-124">Verhindert, dass das System kaufmännische und Zeichen aus einer Zeichenfolge entfernt oder eine Zeichenfolge mit einem Tabstopp Zeichen beendet.</span><span class="sxs-lookup"><span data-stu-id="69091-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="69091-125">Ohne diesen Stil entfernt das System automatisch kaufmännische und Zeichen und beendet eine Zeichenfolge beim ersten Tabstopp Zeichen.</span><span class="sxs-lookup"><span data-stu-id="69091-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="69091-126">Dies ermöglicht es einer Anwendung, dieselbe Zeichenfolge wie ein Menü Element und als Text in einem QuickInfo-Steuerelement zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="69091-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="69091-127"><dt>**TTS \_ usevisualstyle**</dt></span><span class="sxs-lookup"><span data-stu-id="69091-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="69091-128">Verwendet Hyperlinks mit einem Thema.</span><span class="sxs-lookup"><span data-stu-id="69091-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="69091-129">Mit dem Design werden die Stile für alle Links in der QuickInfo definiert.</span><span class="sxs-lookup"><span data-stu-id="69091-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="69091-130">Dieser Stil erfordert immer \_ die Festlegung von ttf-Parametern.</span><span class="sxs-lookup"><span data-stu-id="69091-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="69091-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69091-131">Remarks</span></span>

<span data-ttu-id="69091-132">Ein QuickInfo-Steuerelement verfügt immer über die \_ Fenster Stile "WS Popup" und "WS \_ Ex \_ Tool Window", unabhängig davon, ob Sie diese beim Erstellen des Steuer Elements angeben</span><span class="sxs-lookup"><span data-stu-id="69091-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="69091-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69091-133">Requirements</span></span>



| <span data-ttu-id="69091-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69091-134">Requirement</span></span> | <span data-ttu-id="69091-135">Wert</span><span class="sxs-lookup"><span data-stu-id="69091-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69091-136">Header</span><span class="sxs-lookup"><span data-stu-id="69091-136">Header</span></span><br/> | <dl> <span data-ttu-id="69091-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="69091-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





