---
title: Igathernotify addscope (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify addscope (deprecated)-Methode
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Addscope (veraltet) Methode Legacy-Windows-Umgebungs Features
- Addscope (veraltet) Methode Legacy-Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, addscope (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353009"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="4cf63-107">Igathernotify:: addscope (deprecated)-Methode</span><span class="sxs-lookup"><span data-stu-id="4cf63-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="4cf63-108">\[**Addscope** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert werden oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="4cf63-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="4cf63-109">Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.</span><span class="sxs-lookup"><span data-stu-id="4cf63-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="4cf63-110">Fügt die Startseite oder die URL hinzu, die Sie überwachen.</span><span class="sxs-lookup"><span data-stu-id="4cf63-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="4cf63-111">Dadurch wird eine inkrementelle durch Forstung initiiert, wenn eine Verbindung hergestellt wird</span><span class="sxs-lookup"><span data-stu-id="4cf63-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf63-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cf63-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="4cf63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cf63-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf63-114">*bstrauscope* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cf63-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf63-115">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4cf63-115">Type: **BSTR**</span></span>

<span data-ttu-id="4cf63-116">Eine Zeichenfolge, die die zu überwachende Startseite oder den zu überwachenden urlangibt.</span><span class="sxs-lookup"><span data-stu-id="4cf63-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf63-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cf63-117">Return value</span></span>

<span data-ttu-id="4cf63-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4cf63-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf63-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cf63-119">Remarks</span></span>

<span data-ttu-id="4cf63-120">Beim Aufrufen dieser Methode wird ein inkrementelles Crawl gestartet, wenn eine Verbindung mit dem Speicher</span><span class="sxs-lookup"><span data-stu-id="4cf63-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="4cf63-121">Danach wird davon ausgegangen, dass alle URL-Änderungen nach dem ersten Update durch eine Benachrichtigung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="4cf63-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
