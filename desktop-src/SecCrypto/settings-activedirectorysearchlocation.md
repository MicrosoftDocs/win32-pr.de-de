---
description: Legt den Active Directory Suchspeicherort fest oder ruft ihn ab.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Settings. activedirectoriysearchlocation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364768"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="181a9-103">Settings. activedirectoriysearchlocation (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="181a9-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="181a9-104">\[Die **activedirector ysearchlocation** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="181a9-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="181a9-105">Die **activedirector ysearchlocation** -Eigenschaft legt den Active Directory Suchspeicherort fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="181a9-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="181a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="181a9-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="181a9-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="181a9-107">Property value</span></span>

<span data-ttu-id="181a9-108">Ein Wert der CAPICOM-Enumeration für den [**\_ Active \_ Directory- \_ \_ Suchort**](capicom-active-directory-search-location.md) , der den Such Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="181a9-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="181a9-109">Der Standardwert ist CAPICOM \_ Search \_ any.</span><span class="sxs-lookup"><span data-stu-id="181a9-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="181a9-110">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="181a9-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="181a9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="181a9-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="181a9-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="181a9-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="181a9-113"><dt>**CAPICOM- \_ Suche \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="181a9-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="181a9-114">Suchen Sie alle verfügbaren Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="181a9-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="181a9-115"><dt>**\_ \_ Standard \_ Domäne für CAPICOM-Suche**</dt></span><span class="sxs-lookup"><span data-stu-id="181a9-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="181a9-116">Nur die Standard Domäne suchen.</span><span class="sxs-lookup"><span data-stu-id="181a9-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="181a9-117"><dt>**CAPICOM- \_ Suche ( \_ globaler \_ Katalog)**</dt></span><span class="sxs-lookup"><span data-stu-id="181a9-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="181a9-118">Durchsuchen Sie nur den globalen Katalog.</span><span class="sxs-lookup"><span data-stu-id="181a9-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="181a9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="181a9-119">Requirements</span></span>



| <span data-ttu-id="181a9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="181a9-120">Requirement</span></span> | <span data-ttu-id="181a9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="181a9-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="181a9-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="181a9-122">Redistributable</span></span><br/> | <span data-ttu-id="181a9-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="181a9-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="181a9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="181a9-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="181a9-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="181a9-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181a9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="181a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181a9-127">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="181a9-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




