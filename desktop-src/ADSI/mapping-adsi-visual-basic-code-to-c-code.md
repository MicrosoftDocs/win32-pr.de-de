---
title: Zuordnung von ADSI-Visual Basic Code zu C++-Code
description: ADSI besteht aus mehr als 50 Schnittstellen.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340193"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="0710a-103">Zuordnung von ADSI-Visual Basic Code zu C++-Code</span><span class="sxs-lookup"><span data-stu-id="0710a-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="0710a-104">ADSI besteht aus mehr als 50 Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0710a-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="0710a-105">Die meisten Verzeichnis Vorgänge können nur mit fünf Schnittstellen abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0710a-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="0710a-106">Sie lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0710a-106">They are:</span></span>

-   [<span data-ttu-id="0710a-107">**Iadsopendsobject**</span><span class="sxs-lookup"><span data-stu-id="0710a-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="0710a-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="0710a-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="0710a-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="0710a-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="0710a-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="0710a-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="0710a-111">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="0710a-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="0710a-112">In der folgenden Tabelle sind die Zuordnungen von ADSI VB/VSB-Code zu C++-Code aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0710a-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="0710a-113">Beachten Sie, dass es sich hierbei nicht um eine komplette Liste handelt.</span><span class="sxs-lookup"><span data-stu-id="0710a-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="0710a-114">VSB-Code</span><span class="sxs-lookup"><span data-stu-id="0710a-114">VBS Code</span></span>                           | <span data-ttu-id="0710a-115">VC-Code</span><span class="sxs-lookup"><span data-stu-id="0710a-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0710a-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="0710a-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="0710a-117">HR = ADsGetObject ()</span><span class="sxs-lookup"><span data-stu-id="0710a-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="0710a-118">obj. Legen Sie obj ab. "Obj" erhalten. Übergeordneten</span><span class="sxs-lookup"><span data-stu-id="0710a-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="0710a-119">IADs oder IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="0710a-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="0710a-120">obj. Erstellen Sie obj. Löschen Sie obj. Muvehere</span><span class="sxs-lookup"><span data-stu-id="0710a-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="0710a-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="0710a-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="0710a-122">For each...</span><span class="sxs-lookup"><span data-stu-id="0710a-122">For each…</span></span> <span data-ttu-id="0710a-123">in...</span><span class="sxs-lookup"><span data-stu-id="0710a-123">in…</span></span>                      | <span data-ttu-id="0710a-124">Adsbuildenvererator () adseneneratenext ()</span><span class="sxs-lookup"><span data-stu-id="0710a-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="0710a-125">Verbindung, Befehl, Recordset</span><span class="sxs-lookup"><span data-stu-id="0710a-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="0710a-126">IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0710a-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="0710a-127">Sicherheits Beschreibung, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="0710a-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="0710a-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="0710a-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




