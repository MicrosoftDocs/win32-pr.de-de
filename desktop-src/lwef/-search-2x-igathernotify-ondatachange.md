---
title: Igathernotify OnDataChange (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify OnDataChange (deprecated)-Methode
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (veraltet) Methode ältere Windows-Umgebungs Features
- OnDataChange (veraltet) Methode ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, OnDataChange (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361156"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="e9a6a-107">Igathernotify:: OnDataChange (deprecated)-Methode</span><span class="sxs-lookup"><span data-stu-id="e9a6a-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="e9a6a-108">\[**OnDataChange** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="e9a6a-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="e9a6a-109">Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="e9a6a-110">Diese Methode benachrichtigt den Indexer von Daten, die sich geändert haben.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="e9a6a-111">Beim Senden der Benachrichtigung an den Indexer enthält Sie den Typ der Änderung, die physische Adresse und die logische Adresse.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a6a-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a6a-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="e9a6a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9a6a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a6a-114">*Echange-Empfehlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a6a-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a6a-115">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="e9a6a-115">Type: **long**</span></span>

<span data-ttu-id="e9a6a-116">Ein-Enumerationswert, der den Typ der Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="e9a6a-117">*bstrauphysicaladdress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a6a-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a6a-118">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e9a6a-118">Type: **BSTR**</span></span>

<span data-ttu-id="e9a6a-119">Die physische Adresse des geänderten Elements.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="e9a6a-120">*bstraulogicaladdress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a6a-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a6a-121">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e9a6a-121">Type: **BSTR**</span></span>

<span data-ttu-id="e9a6a-122">Die logische Adresse des geänderten Elements.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a6a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9a6a-123">Return value</span></span>

<span data-ttu-id="e9a6a-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e9a6a-124">This method does not return a value.</span></span>

 

 
