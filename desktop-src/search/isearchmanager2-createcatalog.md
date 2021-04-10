---
description: Erstellt einen neuen benutzerdefinierten Katalog im Windows Search-Indexer und gibt einen Verweis darauf zurück.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2:: kreatecatalog-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214450"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="1a7ba-103">ISearchManager2:: kreatecatalog-Methode</span><span class="sxs-lookup"><span data-stu-id="1a7ba-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="1a7ba-104">Erstellt einen neuen benutzerdefinierten Katalog im Windows Search-Indexer und gibt einen Verweis darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a7ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a7ba-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="1a7ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a7ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7ba-107">*pszcatalog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a7ba-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a7ba-108">Typ: **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a7ba-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a7ba-109">Der Name des zu erstellenden Katalogs.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-109">Name of catalog to create.</span></span> <span data-ttu-id="1a7ba-110">Kann ein beliebiger Name sein, der vom Aufrufer ausgewählt wird, darf nur alphanumerische Zeichen und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="1a7ba-111">*ppcatalogmanager* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a7ba-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a7ba-112">Typ: **[ **isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="1a7ba-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="1a7ba-113">Bei Erfolg wird ein Verweis auf den erstellten Katalog als [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Schnittstellen Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="1a7ba-114">Das Release () muss für diese Schnittstelle aufgerufen werden, nachdem die aufrufende Anwendung die Verwendung der Anwendung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7ba-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a7ba-115">Return value</span></span>

<span data-ttu-id="1a7ba-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a7ba-116">Type: **HRESULT**</span></span>

<span data-ttu-id="1a7ba-117">HRESULT, das den Status des Vorgangs angibt:</span><span class="sxs-lookup"><span data-stu-id="1a7ba-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="1a7ba-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1a7ba-118">Return code</span></span>                                                                             | <span data-ttu-id="1a7ba-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a7ba-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a7ba-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7ba-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1a7ba-121">Der Katalog war nicht bereits vorhanden und wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="1a7ba-122">Verweis auf den zurückgegebenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="1a7ba-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7ba-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1a7ba-124">Der Katalog war bereits vorhanden, Verweis auf den zurückgegebenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="1a7ba-125">HRESULT-Fehler: Fehler beim Erstellen des Katalogs oder ungültige Argumente.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a7ba-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a7ba-126">Remarks</span></span>

<span data-ttu-id="1a7ba-127">Wird aufgerufen, um einen neuen Katalog im Windows Search-Indexer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="1a7ba-128">Nach der Erstellung können die Methoden im zurückgegebenen [**isearchcatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Manager zum Hinzufügen von zu indizierenden Speicherorten, zum Überwachen des Indizierungs Prozesses und zum Erstellen von Abfragen verwendet werden, die an den Indexer gesendet und Ergebnisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a7ba-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="1a7ba-129">Weitere Informationen finden Sie in der Dokumentation zum Verwalten des Indexes: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="1a7ba-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7ba-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a7ba-130">Requirements</span></span>



| <span data-ttu-id="1a7ba-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a7ba-131">Requirement</span></span> | <span data-ttu-id="1a7ba-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1a7ba-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a7ba-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a7ba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7ba-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a7ba-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="1a7ba-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a7ba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7ba-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a7ba-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a7ba-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a7ba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7ba-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="1a7ba-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
