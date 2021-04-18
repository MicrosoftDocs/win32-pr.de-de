---
title: Interaktion mit WinEvents
description: Die Lauf Zeit der dynamischen Anmerkung sendet keine WinEvents. Es liegt in der Verantwortung des Annotator, bei Bedarf geeignete Ereignisse zu senden. Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass diese nach der Anmerkung gesendet werden.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106339256"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="ce26a-104">Interaktion mit WinEvents</span><span class="sxs-lookup"><span data-stu-id="ce26a-104">Interaction with WinEvents</span></span>

<span data-ttu-id="ce26a-105">Die Lauf Zeit der dynamischen Anmerkung sendet keine [WinEvents](winevents-infrastructure.md). Es liegt in der Verantwortung des Annotator, bei Bedarf geeignete Ereignisse zu senden.</span><span class="sxs-lookup"><span data-stu-id="ce26a-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="ce26a-106">Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass diese nach der Anmerkung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce26a-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="ce26a-107">Wenn Sie z. b. [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) verwenden, um die [**Name**](name-property.md) -Eigenschaft eines Elements festzulegen, senden Sie ein [**Ereignis \_ Objekt \_ NameChange**](event-constants.md) -Ereignis für dieses Objekt, nachdem **SetPropValue** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ce26a-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="ce26a-108">Wenn Sie jedoch [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) verwenden, um die ValueMap für einen Schieberegler festzulegen, sind keine Ereignisse erforderlich, da durch das Festlegen von ValueMap der Wert des Schiebereglers nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ce26a-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




