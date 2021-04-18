---
title: Überladen von IPropertyNotifySink
description: Überladen von IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388640"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="4f334-103">Überladen von IPropertyNotifySink</span><span class="sxs-lookup"><span data-stu-id="4f334-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="4f334-104">Viele ActiveX-Steuerelement Container implementieren ein nicht modalem Eigenschaften Browserfenster.</span><span class="sxs-lookup"><span data-stu-id="4f334-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="4f334-105">Wenn die Eigenschaften eines Steuer Elements über die Eigenschaften Seiten des-Steuer Elements geändert werden, können die Eigenschaften des Steuer Elements nicht mehr mit der Ansicht des Containers synchronisiert werden (das Steuerelement ist natürlich immer richtig).</span><span class="sxs-lookup"><span data-stu-id="4f334-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="4f334-106">Um sicherzustellen, dass Sie immer über die aktuellen Werte für die Eigenschaften eines Steuer Elements verfügt, kann ein ActiveX-Steuerelement Container die [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) -Schnittstelle (Datenbindung) überladen und damit darüber benachrichtigt werden, dass sich eine Steuerelement Eigenschaft geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4f334-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="4f334-107">Diese Technik ist optional und nicht erforderlich für ActiveX-Steuerelement Container oder ActiveX-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="4f334-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="4f334-108">Beachten Sie, dass ein Steuerelement [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) nur für die Datenbindung verwenden soll. Es ist kostenlos, [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) für beide Zwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f334-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




