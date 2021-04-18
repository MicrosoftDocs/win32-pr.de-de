---
title: Igathernotify init (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify init (deprecated)-Methode
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (veraltet) Methode ältere Windows-Umgebungs Features
- Init (deprecated), ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, init (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351883"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="bd6af-107">Igathernotify:: init (deprecated)-Methode</span><span class="sxs-lookup"><span data-stu-id="bd6af-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="bd6af-108">\[**Init** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="bd6af-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="bd6af-109">Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.</span><span class="sxs-lookup"><span data-stu-id="bd6af-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="bd6af-110">Initialisiert die gathererschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bd6af-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="bd6af-111">Gibt außerdem den zu benachrichtigenden Index und den zu überwachenden Anwendungs Speicher an.</span><span class="sxs-lookup"><span data-stu-id="bd6af-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6af-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd6af-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="bd6af-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd6af-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6af-114">*bstrapplikation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd6af-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6af-115">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bd6af-115">Type: **BSTR**</span></span>

<span data-ttu-id="bd6af-116">Eine Zeichenfolge, die die Zielanwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="bd6af-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="bd6af-117">*bstrinproject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd6af-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6af-118">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bd6af-118">Type: **BSTR**</span></span>

<span data-ttu-id="bd6af-119">Eine Zeichenfolge, die den Namen des Indexers angibt, an den gathererinformationen übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd6af-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="bd6af-120">*varscopesbstrauarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd6af-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6af-121">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bd6af-121">Type: **variant**</span></span>

<span data-ttu-id="bd6af-122">Optionaler Parameter, der es Ihnen ermöglicht, ein Array von Bereichen zu übergeben, die initialisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd6af-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6af-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd6af-123">Return value</span></span>

<span data-ttu-id="bd6af-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd6af-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6af-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd6af-125">Remarks</span></span>

<span data-ttu-id="bd6af-126">Initialisieren Sie mit Application = "rsapp", Project = "myIndex".</span><span class="sxs-lookup"><span data-stu-id="bd6af-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
