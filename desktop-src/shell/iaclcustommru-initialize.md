---
description: Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten (MRU) aus der Registrierung.
title: IACLCustomMRU::Initialize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841231"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="85a38-103">IACLCustomMRU::Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="85a38-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="85a38-104">Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten (MRU) aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="85a38-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85a38-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="85a38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a38-107">*pwszMRURegKey* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="85a38-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a38-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="85a38-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="85a38-109">Ein Zeiger auf einen Puffer, der den Registrierungsschlüssel mit den Zeichenfolgen für die MRU-Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="85a38-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="85a38-110">*dwMax* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="85a38-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a38-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="85a38-111">Type: **DWORD**</span></span>

<span data-ttu-id="85a38-112">Die maximale Anzahl von Einträgen, die aus *pwszMRURegKey* entnommen werden können.</span><span class="sxs-lookup"><span data-stu-id="85a38-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a38-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85a38-113">Return value</span></span>

<span data-ttu-id="85a38-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85a38-114">Type: **HRESULT**</span></span>

<span data-ttu-id="85a38-115">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85a38-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85a38-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85a38-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a38-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85a38-117">Requirements</span></span>



| <span data-ttu-id="85a38-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85a38-118">Requirement</span></span> | <span data-ttu-id="85a38-119">Wert</span><span class="sxs-lookup"><span data-stu-id="85a38-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85a38-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85a38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85a38-121">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85a38-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="85a38-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85a38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85a38-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85a38-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




