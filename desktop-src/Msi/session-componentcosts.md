---
description: Die componentcosts-Eigenschaft des Session-Objekts gibt ein RecordList-Objekt zurück, das den für die Installation einer Komponente erforderlichen Speicherplatz pro Laufwerk auflistet.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Session. componentcosts (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369689"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="bec77-103">Session. componentcosts (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bec77-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="bec77-104">Die componentcosts-Eigenschaft des [**Session**](session-object.md) -Objekts gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den für die Installation einer Komponente erforderlichen Speicherplatz pro Laufwerk auflistet.</span><span class="sxs-lookup"><span data-stu-id="bec77-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="bec77-105">Diese Informationen werden von der Benutzeroberfläche verwendet, um den erforderlichen Speicherplatz für alle Laufwerke anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bec77-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="bec77-106">Die zurückgegebenen Speicherplatz Kosten liegen in Vielfachen von 512 Bytes.</span><span class="sxs-lookup"><span data-stu-id="bec77-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="bec77-107">Die componentcosts-Eigenschaft sollte nur verwendet werden, nachdem das Installationsprogramm die [Datei Kosten](file-costing.md) und nach der [costfinalize-Aktion](costfinalize-action.md)abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="bec77-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="bec77-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bec77-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec77-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec77-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="bec77-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bec77-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bec77-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bec77-111">Remarks</span></span>

<span data-ttu-id="bec77-112">Um die Gesamtkosten zu erhalten, fügen Sie die Kosten für alle Komponenten zuzüglich der Kosten für den Installer-Engine (Component = "") hinzu.</span><span class="sxs-lookup"><span data-stu-id="bec77-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="bec77-113">Componentcosts gibt ein [**RecordList-Objekt**](recordlist-object.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="bec77-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="bec77-114">Jeder Datensatz im zurückgegebenen RecordList-Objekt verfügt über die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="bec77-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="bec77-115">Feld</span><span class="sxs-lookup"><span data-stu-id="bec77-115">Field</span></span> | <span data-ttu-id="bec77-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec77-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="bec77-117">1</span><span class="sxs-lookup"><span data-stu-id="bec77-117">1</span></span>     | <span data-ttu-id="bec77-118">Volume/Laufwerks Name</span><span class="sxs-lookup"><span data-stu-id="bec77-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="bec77-119">2</span><span class="sxs-lookup"><span data-stu-id="bec77-119">2</span></span>     | <span data-ttu-id="bec77-120">Der endgültige Speicherplatz Kosten in Vielfachen von 512 Bytes.</span><span class="sxs-lookup"><span data-stu-id="bec77-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="bec77-121">3</span><span class="sxs-lookup"><span data-stu-id="bec77-121">3</span></span>     | <span data-ttu-id="bec77-122">Temporäre Speicherplatz Kosten in Vielfachen von 512 Bytes.</span><span class="sxs-lookup"><span data-stu-id="bec77-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bec77-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bec77-123">Requirements</span></span>



| <span data-ttu-id="bec77-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bec77-124">Requirement</span></span> | <span data-ttu-id="bec77-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bec77-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec77-126">Version</span><span class="sxs-lookup"><span data-stu-id="bec77-126">Version</span></span><br/> | <span data-ttu-id="bec77-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bec77-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bec77-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bec77-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bec77-129">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="bec77-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bec77-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bec77-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="bec77-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bec77-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bec77-132">IID</span><span class="sxs-lookup"><span data-stu-id="bec77-132">IID</span></span><br/>     | <span data-ttu-id="bec77-133">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bec77-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




