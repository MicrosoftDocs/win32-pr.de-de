---
description: Stellt die Funktion zum erneuten Zuordnen von Datei Versions Verläufen dar, die es einem Benutzer ermöglicht, eine Beziehung mit einem Sicherungs Ziel wiederherzustellen, das in der Vergangenheit von demselben Benutzer verwendet wurde. Die erneute Zuordnung erfolgt durch Aufrufen der Methoden der ifhreassociation-Schnittstelle.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Fhreassociation-Klasse (fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343173"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="c2b0c-104">Klasse "Klasse"</span><span class="sxs-lookup"><span data-stu-id="c2b0c-104">FhReassociation class</span></span>

<span data-ttu-id="c2b0c-105">Stellt die Funktion zum erneuten Zuordnen von Datei Versions Verläufen dar, die es einem Benutzer ermöglicht, eine Beziehung mit einem Sicherungs Ziel wiederherzustellen, das in der Vergangenheit von demselben Benutzer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="c2b0c-106">Die erneute Zuordnung erfolgt durch Aufrufen der Methoden der [**ifhreassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c2b0c-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="c2b0c-107">When to implement</span></span>

<span data-ttu-id="c2b0c-108">Die API für den Datei Versionsverlauf implementiert diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-108">The File History API implements this class.</span></span> <span data-ttu-id="c2b0c-109">Verwenden Sie die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b0c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2b0c-110">Requirements</span></span>



| <span data-ttu-id="c2b0c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2b0c-111">Requirement</span></span> | <span data-ttu-id="c2b0c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c2b0c-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b0c-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2b0c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b0c-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2b0c-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2b0c-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2b0c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b0c-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2b0c-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2b0c-117">Header</span><span class="sxs-lookup"><span data-stu-id="c2b0c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2b0c-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b0c-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2b0c-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c2b0c-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2b0c-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2b0c-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
