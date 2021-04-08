---
title: Iwmdrmprovider-Schnittstelle
description: Die iwmdrmprovider-Schnittstelle stellt eine Methode bereit, mit der die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client erstellt werden. Sie können einen Zeiger auf eine Instanz dieser Schnittstelle abrufen, indem Sie die wmdrmcreateprovider-Funktion aufrufen.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Iwmdrmprovider-Schnittstelle Windows Media-Format
- Iwmdrmprovider-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729216"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="be538-105">Iwmdrmprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="be538-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="be538-106">Die **iwmdrmprovider** -Schnittstelle stellt eine Methode bereit, mit der die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="be538-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="be538-107">Sie können einen Zeiger auf eine Instanz dieser Schnittstelle abrufen, indem Sie die [**wmdrmcreateprovider**](wmdrmcreateprovider.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="be538-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="be538-108">Zum Abrufen eines Zeigers auf eine Instanz dieser Schnittstelle, die sichere Objekte erstellen kann, müssen Sie die [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="be538-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="be538-109">Member</span><span class="sxs-lookup"><span data-stu-id="be538-109">Members</span></span>

<span data-ttu-id="be538-110">Die **iwmdrmprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="be538-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be538-111">**Iwmdrmprovider** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be538-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="be538-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="be538-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be538-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="be538-113">Methods</span></span>

<span data-ttu-id="be538-114">Die **iwmdrmprovider** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="be538-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="be538-115">Methode</span><span class="sxs-lookup"><span data-stu-id="be538-115">Method</span></span>                                              | <span data-ttu-id="be538-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be538-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be538-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="be538-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="be538-118">Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.</span><span class="sxs-lookup"><span data-stu-id="be538-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="be538-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be538-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be538-120">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="be538-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

