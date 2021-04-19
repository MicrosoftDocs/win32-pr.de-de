---
title: Syslink-Steuerelement Stile (kommctrl. h)
description: Die folgenden Stil Konstanten werden verwendet, wenn Syslink-Steuerelemente erstellt werden.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373744"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="6be2d-103">Syslink-Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="6be2d-103">SysLink Control Styles</span></span>

<span data-ttu-id="6be2d-104">Die folgenden Stil Konstanten werden verwendet, wenn Syslink-Steuerelemente erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6be2d-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="6be2d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="6be2d-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="6be2d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6be2d-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="6be2d-107"><dt>**LWS \_ transparent**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="6be2d-108">Der Hintergrund Mischungs Modus ist transparent.</span><span class="sxs-lookup"><span data-stu-id="6be2d-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="6be2d-109"><dt>**LWS \_ Ignorereturn**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="6be2d-110">Wenn der Link den Tastaturfokus besitzt und der Benutzer die EINGABETASTE drückt, wird der Tastatur Strich vom Steuerelement ignoriert und an das Dialogfeld Host übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6be2d-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="6be2d-111"><dt>**LWS \_ NoPrefix**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="6be2d-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6be2d-112">**Windows Vista**.</span></span> <span data-ttu-id="6be2d-113">Wenn der Text ein kaufmännisches und-Zeichen enthält, wird es als Literalzeichen und nicht als Präfix für eine Tastenkombination behandelt.</span><span class="sxs-lookup"><span data-stu-id="6be2d-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="6be2d-114"><dt>**LWS \_ Usevisualstyle**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="6be2d-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6be2d-115">**Windows Vista**.</span></span> <span data-ttu-id="6be2d-116">Der Link wird im aktuellen visuellen Stil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6be2d-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="6be2d-117"><dt>**LWS \_ usecustomtext**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="6be2d-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6be2d-118">**Windows Vista**.</span></span> <span data-ttu-id="6be2d-119">Eine [nm- \_ CustomText](nm-customtext.md) -Benachrichtigung wird gesendet, wenn das Steuerelement gezeichnet wird, damit die Anwendung Text dynamisch bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6be2d-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="6be2d-120"><dt>**LWS \_ Rechts**</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="6be2d-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6be2d-121">**Windows Vista**.</span></span> <span data-ttu-id="6be2d-122">Der Text wird rechtsbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="6be2d-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="6be2d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6be2d-123">Requirements</span></span>



| <span data-ttu-id="6be2d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6be2d-124">Requirement</span></span> | <span data-ttu-id="6be2d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6be2d-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6be2d-126">Header</span><span class="sxs-lookup"><span data-stu-id="6be2d-126">Header</span></span><br/> | <dl> <span data-ttu-id="6be2d-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be2d-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





