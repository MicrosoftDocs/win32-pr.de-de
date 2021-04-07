---
title: Iwmdrmnonsilentlicenseaquisition-Schnittstelle
description: Die iwmdrmnonsilentlicenseaquisition-Schnittstelle stellt Methoden bereit, die den Erwerb von Lizenzen ermöglichen, die einen Benutzereingriff erfordern. Diese Schnittstelle kann durch die Ausführung eines nicht automatischen Lizenz Erwerbs abgerufen werden.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format
- Iwmdrmnonsilentlicenseaquisition Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728712"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="43289-105">Iwmdrmnonsilentlicenseaquisition-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="43289-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="43289-106">Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle stellt Methoden bereit, die den Erwerb von Lizenzen ermöglichen, die einen Benutzereingriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="43289-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="43289-107">Diese Schnittstelle kann durch die Ausführung eines nicht automatischen Lizenz Erwerbs abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="43289-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="43289-108">Nachdem Sie [**iwmdrmlicensmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) aufgerufen haben, wird ein **mewmdrmlicenabacquisitionabgeschlossene** -Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="43289-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="43289-109">Aufrufen der **imfmediaevent:: GetValue** -Methode des Ereignisses zum Abrufen eines Zeigers auf eine **IUnknown** -Schnittstelle, die für einen Zeiger auf eine Instanz dieser Schnittstelle abgefragt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43289-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="43289-110">Member</span><span class="sxs-lookup"><span data-stu-id="43289-110">Members</span></span>

<span data-ttu-id="43289-111">Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43289-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43289-112">**Iwmdrmnonsilentlicenseaquisition** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43289-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="43289-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="43289-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43289-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="43289-114">Methods</span></span>

<span data-ttu-id="43289-115">Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="43289-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="43289-116">Methode</span><span class="sxs-lookup"><span data-stu-id="43289-116">Method</span></span>                                                                | <span data-ttu-id="43289-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43289-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="43289-118">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="43289-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="43289-119">Ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43289-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="43289-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="43289-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="43289-121">Ruft die URL ab, an die die Lizenz Aufforderung gepostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43289-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="43289-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43289-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43289-123">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="43289-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="43289-124">**Nicht automatische Lizenz Beschaffung**</span><span class="sxs-lookup"><span data-stu-id="43289-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

