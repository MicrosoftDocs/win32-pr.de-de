---
description: Gibt den Speicherort an, der nach einem Active Directory Zertifikat Speicher gesucht werden soll.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351237"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="930e7-103">CAPICOM- \_ Active \_ Directory- \_ \_ Suchspeicherort-Enumeration</span><span class="sxs-lookup"><span data-stu-id="930e7-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="930e7-104">Der Enumerationstyp " **CAPICOM \_ Active \_ Directory- \_ \_ Suchort** " gibt den Speicherort an, der nach einem Active Directory [*Zertifikat Speicher*](../secgloss/c-gly.md)gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="930e7-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="930e7-105">Member</span><span class="sxs-lookup"><span data-stu-id="930e7-105">Members</span></span>



| <span data-ttu-id="930e7-106">Member</span><span class="sxs-lookup"><span data-stu-id="930e7-106">Member</span></span>                               | <span data-ttu-id="930e7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="930e7-107">Description</span></span>                                  | <span data-ttu-id="930e7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="930e7-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="930e7-109">**CAPICOM- \_ Suche \_ Any**</span><span class="sxs-lookup"><span data-stu-id="930e7-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="930e7-110">Durchsucht alle verfügbaren Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="930e7-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="930e7-111">0</span><span class="sxs-lookup"><span data-stu-id="930e7-111">0</span></span>     |
| <span data-ttu-id="930e7-112">**CAPICOM- \_ Suche ( \_ globaler \_ Katalog)**</span><span class="sxs-lookup"><span data-stu-id="930e7-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="930e7-113">Durchsucht nur den globalen Katalog.</span><span class="sxs-lookup"><span data-stu-id="930e7-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="930e7-114">1</span><span class="sxs-lookup"><span data-stu-id="930e7-114">1</span></span>     |
| <span data-ttu-id="930e7-115">**\_ \_ Standard \_ Domäne für CAPICOM-Suche**</span><span class="sxs-lookup"><span data-stu-id="930e7-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="930e7-116">Durchsucht nur die Standard Domäne.</span><span class="sxs-lookup"><span data-stu-id="930e7-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="930e7-117">2</span><span class="sxs-lookup"><span data-stu-id="930e7-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="930e7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="930e7-118">Remarks</span></span>

<span data-ttu-id="930e7-119">Dieser Enumerationstyp wird von der folgenden Eigenschaft verwendet:</span><span class="sxs-lookup"><span data-stu-id="930e7-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="930e7-120">**Settings. activedirectoriysearchlocation**</span><span class="sxs-lookup"><span data-stu-id="930e7-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="930e7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="930e7-121">Requirements</span></span>



| <span data-ttu-id="930e7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="930e7-122">Requirement</span></span> | <span data-ttu-id="930e7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="930e7-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="930e7-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="930e7-124">Redistributable</span></span><br/> | <span data-ttu-id="930e7-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="930e7-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="930e7-126">Header</span><span class="sxs-lookup"><span data-stu-id="930e7-126">Header</span></span><br/>          | <dl> <span data-ttu-id="930e7-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="930e7-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
