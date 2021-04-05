---
title: Iwmdrmindividualizationstatus-Schnittstelle
description: Die iwmdrmindividualizationstatus-Schnittstelle ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung. Diese Schnittstelle wird mit mewmdrmindividualizationprogress-Ereignissen geliefert.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Iwmdrmindividualizationstatus-Schnittstelle Windows Media-Format
- Iwmdrmindividualizationstatus Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948991"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="5f7bc-105">Iwmdrmindividualizationstatus-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5f7bc-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="5f7bc-106">Die **iwmdrmindividualizationstatus** -Schnittstelle ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="5f7bc-107">Diese Schnittstelle wird mit mewmdrmindividualizationprogress-Ereignissen geliefert.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="5f7bc-108">Viele derartige Ereignisse werden zwischen einem Aufruf von [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) und dem Abschluss des Individualisierungs Prozesses generiert, der durch die Generierung eines **mewmdrmindividualizationabgeschlossene** -Ereignisses signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="5f7bc-109">Wenn Sie einen Zeiger auf eine Instanz der **iwmdrmindividualizationstatus** -Schnittstelle abrufen möchten, müssen Sie zuerst die **imfmediaevent:: GetValue** -Methode des Fortschritts Ereignisses aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="5f7bc-110">Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das die **iwmdrmindividualizationstatus** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5f7bc-111">Member</span><span class="sxs-lookup"><span data-stu-id="5f7bc-111">Members</span></span>

<span data-ttu-id="5f7bc-112">Die **iwmdrmindividualizationstatus** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5f7bc-113">**Iwmdrmindividualizationstatus** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f7bc-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="5f7bc-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="5f7bc-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f7bc-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="5f7bc-115">Methods</span></span>

<span data-ttu-id="5f7bc-116">Die **iwmdrmindividualizationstatus** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="5f7bc-117">Methode</span><span class="sxs-lookup"><span data-stu-id="5f7bc-117">Method</span></span>                                                       | <span data-ttu-id="5f7bc-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f7bc-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="5f7bc-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="5f7bc-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="5f7bc-120">Ruft ausführliche Informationen zur Individualisierung ab.</span><span class="sxs-lookup"><span data-stu-id="5f7bc-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5f7bc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f7bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f7bc-122">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="5f7bc-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

