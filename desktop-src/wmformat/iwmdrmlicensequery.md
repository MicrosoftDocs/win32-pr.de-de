---
title: Iwmdrmlicensequery-Schnittstelle
description: Die iwmdrmlicensequery-Schnittstelle ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format
- Iwmdrmlicensequery Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728713"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="6c3a2-105">Iwmdrmlicensequery-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6c3a2-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="6c3a2-106">Die **iwmdrmlicensequery** -Schnittstelle ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="6c3a2-107">Diese Schnittstelle verwendet die Schlüssel-ID, um Abfragen für den lokalen Lizenz Speicher auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="6c3a2-108">Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="6c3a2-109">Übergeben Sie **IID \_ iwmdrmlicensequery** als *riid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="6c3a2-110">Member</span><span class="sxs-lookup"><span data-stu-id="6c3a2-110">Members</span></span>

<span data-ttu-id="6c3a2-111">Die **iwmdrmlicensequery** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c3a2-112">**Iwmdrmlicensequery** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c3a2-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="6c3a2-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c3a2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c3a2-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c3a2-114">Methods</span></span>

<span data-ttu-id="6c3a2-115">Die **iwmdrmlicensequery** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="6c3a2-116">Methode</span><span class="sxs-lookup"><span data-stu-id="6c3a2-116">Method</span></span>                                                                                | <span data-ttu-id="6c3a2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c3a2-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c3a2-118">**Queryaktionallowed**</span><span class="sxs-lookup"><span data-stu-id="6c3a2-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="6c3a2-119">Fragt den lokalen Lizenz Speicher nach Berechtigungen zum Ausführen von Aktionen anhand der Schlüssel-ID ab.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="6c3a2-120">**Querylicenenstate**</span><span class="sxs-lookup"><span data-stu-id="6c3a2-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="6c3a2-121">Fragt den lokalen Lizenz Speicher nach den Lizenz Zustandsdaten anhand der Schlüssel-ID und spezifischer Rechte ab.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="6c3a2-122">**"Mentactionzugewiesene wedqueryparams"**</span><span class="sxs-lookup"><span data-stu-id="6c3a2-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="6c3a2-123">Legt Umgebungsparameter fest, um die Genauigkeit von Lizenz Abfragen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="6c3a2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c3a2-124">Remarks</span></span>

<span data-ttu-id="6c3a2-125">Die Methoden von **iwmdrmlicensequery** bieten keine Informationen zu einzelnen Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="6c3a2-126">Stattdessen werden die Lizenzdaten durch das DRM-Subsystem aggregiert, bevor die Abfrageergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c3a2-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c3a2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c3a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3a2-128">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="6c3a2-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

