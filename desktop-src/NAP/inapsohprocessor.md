---
title: Inapsohprocessor-Schnittstelle (napprotocol. h)
description: Werden von SHAs verwendet, um den Inhalt von sohantworten und von SHVs zu verarbeiten, um den Inhalt von sohrequests zu verarbeiten.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Inapsohprocessor-Schnittstelle NAP
- Inapsohprocessor-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040132"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="0b6cf-105">Inapsohprocessor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0b6cf-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="0b6cf-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0b6cf-107">Der **inapsohprocessor** stellt Methoden bereit, die von SHAs zum Verarbeiten des Inhalts von [**sohantworten**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs verwendet werden, um den Inhalt von **sohrequests** zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="0b6cf-108">Member</span><span class="sxs-lookup"><span data-stu-id="0b6cf-108">Members</span></span>

<span data-ttu-id="0b6cf-109">Die **inapsohprocessor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b6cf-110">**Inapsohprocessor** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0b6cf-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="0b6cf-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b6cf-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b6cf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b6cf-112">Methods</span></span>

<span data-ttu-id="0b6cf-113">Die **inapsohprocessor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="0b6cf-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0b6cf-114">Method</span></span>                                                                                           | <span data-ttu-id="0b6cf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b6cf-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6cf-116">**Inapsohprocessor:: findnextattribute**</span><span class="sxs-lookup"><span data-stu-id="0b6cf-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="0b6cf-117">Sucht den Speicherort Index des nächsten SoH-Paket Attributs.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="0b6cf-118">**Inapsohprocessor:: GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="0b6cf-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="0b6cf-119">Ruft den Attributtyp und-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="0b6cf-120">**Inapsohprocessor:: getnumofattributes**</span><span class="sxs-lookup"><span data-stu-id="0b6cf-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="0b6cf-121">Ruft die Anzahl der im SoH enthaltenen Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="0b6cf-122">**Inapsohprocessor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="0b6cf-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="0b6cf-123">Initialisiert das SoH-Protokoll Paket und das NAP-System für die Inhalts Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b6cf-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-124">Requirements</span></span>



| <span data-ttu-id="0b6cf-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b6cf-125">Requirement</span></span> | <span data-ttu-id="0b6cf-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0b6cf-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6cf-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b6cf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6cf-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b6cf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b6cf-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b6cf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6cf-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b6cf-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0b6cf-131">Header</span><span class="sxs-lookup"><span data-stu-id="0b6cf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b6cf-132"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b6cf-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b6cf-133">IDL</span><span class="sxs-lookup"><span data-stu-id="0b6cf-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b6cf-134"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b6cf-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="0b6cf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0b6cf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b6cf-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b6cf-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0b6cf-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6cf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6cf-138">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0b6cf-139">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="0b6cf-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

