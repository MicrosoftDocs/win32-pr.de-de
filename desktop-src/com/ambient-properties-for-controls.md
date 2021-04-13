---
title: Ambient-Eigenschaften für Steuerelemente
description: Ambient-Eigenschaften für Steuerelemente
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388430"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="eeddd-103">Ambient-Eigenschaften für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="eeddd-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="eeddd-104">Wenn ein Steuerelement überhaupt Umgebungs Eigenschaften unterstützt, muss es mindestens die Werte der folgenden Ambient-Eigenschaften unter den in der folgenden Tabelle aufgeführten Bedingungen beachten, wobei die Standard-DispIds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eeddd-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="eeddd-105">Ambient-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eeddd-105">Ambient Property</span></span>            | <span data-ttu-id="eeddd-106">DISPID</span><span class="sxs-lookup"><span data-stu-id="eeddd-106">Dispid</span></span>          | <span data-ttu-id="eeddd-107">Kommentare/Bedingungen zur Verwendung</span><span class="sxs-lookup"><span data-stu-id="eeddd-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeddd-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="eeddd-108">LocaleID</span></span><br/>         | <span data-ttu-id="eeddd-109">-705</span><span class="sxs-lookup"><span data-stu-id="eeddd-109">-705</span></span><br/> | <span data-ttu-id="eeddd-110">Wenn das Gebiets Schema für das Steuerelement signifikant ist, z. b. für die Textausgabe</span><span class="sxs-lookup"><span data-stu-id="eeddd-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="eeddd-111">UserMode</span><span class="sxs-lookup"><span data-stu-id="eeddd-111">UserMode</span></span> <br/>        | <span data-ttu-id="eeddd-112">-709</span><span class="sxs-lookup"><span data-stu-id="eeddd-112">-709</span></span><br/> | <span data-ttu-id="eeddd-113">Wenn sich das Steuerelement im Benutzermodus (Entwurfs Modus) und im Lauf Modus anders verhält</span><span class="sxs-lookup"><span data-stu-id="eeddd-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="eeddd-114">Uidead</span><span class="sxs-lookup"><span data-stu-id="eeddd-114">UIDead</span></span><br/>           | <span data-ttu-id="eeddd-115">-710</span><span class="sxs-lookup"><span data-stu-id="eeddd-115">-710</span></span><br/> | <span data-ttu-id="eeddd-116">Wenn das Steuerelement auf Benutzeroberflächen Ereignisse reagiert, sollte es diese Ambient-Eigenschaft berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="eeddd-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="eeddd-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="eeddd-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="eeddd-118">-711</span><span class="sxs-lookup"><span data-stu-id="eeddd-118">-711</span></span><br/> | <span data-ttu-id="eeddd-119">Wenn das Steuerelement die direkte Größe von sich selbst unterstützt</span><span class="sxs-lookup"><span data-stu-id="eeddd-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="eeddd-120">Durch das shoching</span><span class="sxs-lookup"><span data-stu-id="eeddd-120">ShowHatching</span></span><br/>     | <span data-ttu-id="eeddd-121">-712</span><span class="sxs-lookup"><span data-stu-id="eeddd-121">-712</span></span><br/> | <span data-ttu-id="eeddd-122">Wenn das Steuerelement direkte Aktivierung und UI-Aktivierung unterstützt</span><span class="sxs-lookup"><span data-stu-id="eeddd-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="eeddd-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="eeddd-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="eeddd-124">-713</span><span class="sxs-lookup"><span data-stu-id="eeddd-124">-713</span></span><br/> | <span data-ttu-id="eeddd-125">Nur wenn das Steuerelement als OLEMISC \_ acunglikebutton gekennzeichnet ist (d. h., es wird Unterstützung für mnetmonics-Tastatur bereitgestellt, daher muss [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) und [**IOleControl:: onmnetmonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) implementiert werden).</span><span class="sxs-lookup"><span data-stu-id="eeddd-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="eeddd-126">Wie bereits beschrieben, erfordert die Verwendung von Ambients [**sowohl IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) ( [**für OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) als minimal) als auch [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (für [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) und [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="eeddd-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="eeddd-127">Das OLEMISC \_ setclientsitefirst-Bit darf nicht notwendigerweise von einem Container unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="eeddd-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="eeddd-128">In diesen Fällen muss ein Steuerelement auf die Standardwerte für die erforderlichen Umgebungs Eigenschaften zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="eeddd-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeddd-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eeddd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeddd-130">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="eeddd-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





