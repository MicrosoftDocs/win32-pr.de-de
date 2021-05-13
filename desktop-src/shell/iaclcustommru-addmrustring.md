---
description: Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.
title: IACLCustomMRU::AddMRUString-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842001"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="ad449-103">IACLCustomMRU::AddMRUString-Methode</span><span class="sxs-lookup"><span data-stu-id="ad449-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="ad449-104">Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad449-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad449-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad449-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="ad449-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad449-107">*pwszEntry* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad449-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad449-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ad449-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ad449-109">Ein Zeiger auf einen Puffer, der den neuen Eintrag enthält.</span><span class="sxs-lookup"><span data-stu-id="ad449-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad449-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad449-110">Return value</span></span>

<span data-ttu-id="ad449-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad449-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ad449-112">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="ad449-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad449-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad449-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad449-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad449-114">Requirements</span></span>



| <span data-ttu-id="ad449-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad449-115">Requirement</span></span> | <span data-ttu-id="ad449-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ad449-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad449-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad449-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad449-118">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad449-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ad449-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad449-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad449-120">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad449-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




