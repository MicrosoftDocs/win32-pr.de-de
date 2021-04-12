---
title: Igathernotify ondatamove (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify ondatamove (deprecated)-Methode
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Ondatamove (veraltet) Methode ältere Windows-Umgebungs Features
- Ondatamove (veraltet) Methode ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, ondatamove (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353008"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="be251-107">Igathernotify:: ondatamove (deprecated)-Methode</span><span class="sxs-lookup"><span data-stu-id="be251-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="be251-108">\[**Ondatamove** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="be251-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="be251-109">Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.</span><span class="sxs-lookup"><span data-stu-id="be251-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="be251-110">Diese Methode benachrichtigt den Indexer von Daten, die verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="be251-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="be251-111">Wenn die Benachrichtigung an den Indexer gesendet wird, enthält Sie die alte Adresse, die neue Adresse und die logische Adresse.</span><span class="sxs-lookup"><span data-stu-id="be251-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="be251-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="be251-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="be251-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="be251-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be251-114">*echangeadvisesemantics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be251-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be251-115">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="be251-115">Type: **long**</span></span>

<span data-ttu-id="be251-116">Ein Enumerationsparameter, der den Typ der aufgetretenen Verschiebung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="be251-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="be251-117">*bstroldaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be251-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be251-118">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="be251-118">Type: **BSTR**</span></span>

<span data-ttu-id="be251-119">Die alte Adresse des Elements, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="be251-119">The old address of the item that moved.</span></span> <span data-ttu-id="be251-120">Für normale Dateien ist *echangeadvisesematics* **null**.</span><span class="sxs-lookup"><span data-stu-id="be251-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="be251-121">Legen Sie für einen Ordner oder ein Verzeichnis *echangeadvisesematics* auf das Verzeichnis der gthr-Zertifizierungsstellen \_ \_ Semantik fest \_ .</span><span class="sxs-lookup"><span data-stu-id="be251-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="be251-122">*bstrinnewaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be251-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be251-123">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="be251-123">Type: **BSTR**</span></span>

<span data-ttu-id="be251-124">Die neue Adresse des Elements, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="be251-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="be251-125">*bstraulogicaladdress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be251-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be251-126">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="be251-126">Type: **BSTR**</span></span>

<span data-ttu-id="be251-127">Die logische Adresse des Elements, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="be251-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be251-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be251-128">Return value</span></span>

<span data-ttu-id="be251-129">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="be251-129">This method does not return a value.</span></span>

 

 
