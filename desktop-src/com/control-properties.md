---
title: Steuerelement Eigenschaften
description: Steuerelement Eigenschaften
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856900"
---
# <a name="control-properties"></a><span data-ttu-id="6aff1-103">Steuerelement Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aff1-103">Control Properties</span></span>

<span data-ttu-id="6aff1-104">Zusätzlich zu den Eigenschaften, die vom Steuerelement selbst definiert und implementiert werden, umfasst die ActiveX-Steuerelement Technologie auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6aff1-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="6aff1-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aff1-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="6aff1-106">Diese werden vom Container über eine Steuerungs Client Site verfügbar gemacht, um Umgebungs Werte bereitzustellen, die für alle im Container eingebetteten Steuerelemente gelten.</span><span class="sxs-lookup"><span data-stu-id="6aff1-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="6aff1-107">Beispielsweise kann ein Container eine Standard Hintergrundfarbe oder eine Standard Schriftart bereitstellen, die das Steuerelement verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6aff1-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="6aff1-108">Ambient-Eigenschaften werden über **IDispatch** verfügbar gemacht, das für das Site-Objekt eines Containers implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6aff1-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="6aff1-109">Der Container Ruft die [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) -Methode des Steuer Elements auf, wenn einer seiner Ambient-Eigenschaften den Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="6aff1-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="6aff1-110">In der Antwort muss ein Steuerelement möglicherweise seinen eigenen internen oder visuellen Zustand als Antwort aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6aff1-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="6aff1-111">Der Container gibt an, welche Ambient-Eigenschaft mit dem dispid-Parameter geändert wurde, oder übergibt DISPID \_ unknown, um anzugeben, dass mehrere Umgebungs Eigenschaften geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="6aff1-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="6aff1-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Erweiterte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aff1-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="6aff1-113">Diese werden tatsächlich von einem Container implementiert, um die darin enthaltenen Steuerelemente zu umschließen und Container verwaltete Eigenschaften bereitzustellen, die so angezeigt werden, als wären Sie Native Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6aff1-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="6aff1-114">Der Container kann das Steuerelement aggregieren und die erweiterten Eigenschaften hinzufügen, um die Eigenschaften des Steuer Elements zu ergänzen oder zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6aff1-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="6aff1-115">Das aggregierte Objekt wird als erweitertes Steuerelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6aff1-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="6aff1-116">Zum Container wird das erweiterte Steuerelement als Steuerelement angezeigt, und erweiterte Eigenschaften scheinen vom Steuerelement verfügbar gemacht zu werden.</span><span class="sxs-lookup"><span data-stu-id="6aff1-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="6aff1-117">Der Container unterstützt ein erweitertes Steuerelement über die Client Standort Methode [**iolecontrolsite:: getextendedcontrol**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="6aff1-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="6aff1-118">Die **getextendedcontrol** -Methode ermöglicht es Steuerelementen, durch die Site zum erweiterten Steuerelement Objekt zu navigieren, das für Sie durch den Container bereitgestellt wird, wenn der Container dieses Feature unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aff1-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="6aff1-119">Ein Container kann neben den Seiten, die von einem Steuerelement normalerweise über [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)angegeben werden, auch Eigenschaften Seiten für seine erweiterten Steuerelemente anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6aff1-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="6aff1-120">Aus diesem Grund muss ein Steuerelement einen Container bitten, einen Eigenschaften Rahmen anzuzeigen, bevor das Steuerelement versucht, dies selbst zu tun.</span><span class="sxs-lookup"><span data-stu-id="6aff1-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="6aff1-121">Hierfür Ruft das-Steuerelement [**iolecontrolsite:: showpropertyframe**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) auf.</span><span class="sxs-lookup"><span data-stu-id="6aff1-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="6aff1-122">Wenn der Container diese Funktion implementiert, wird der Eigenschafts Rahmen selbst angezeigt. Wenn die Methode einen Fehler zurückgibt, kann das Steuerelement den Eigenschaften Rahmen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6aff1-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="6aff1-123">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6aff1-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6aff1-124">Standard Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aff1-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="6aff1-125">Standard Schriftart Objekt</span><span class="sxs-lookup"><span data-stu-id="6aff1-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="6aff1-126">Standard Bild Objekt</span><span class="sxs-lookup"><span data-stu-id="6aff1-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="6aff1-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6aff1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aff1-128">Steuerungsmethoden</span><span class="sxs-lookup"><span data-stu-id="6aff1-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




