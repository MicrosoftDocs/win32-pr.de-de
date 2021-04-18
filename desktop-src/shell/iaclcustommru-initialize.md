---
description: Lädt eine Liste von Zeichen folgen in die Liste der zuletzt verwendeten (MRU-) Einträge aus der Registrierung.
title: 'Iaclcustommru:: Initialize-Methode'
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
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994631"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="76844-103">Iaclcustommru:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="76844-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="76844-104">Lädt eine Liste von Zeichen folgen in die Liste der zuletzt verwendeten (MRU-) Einträge aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="76844-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="76844-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76844-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="76844-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76844-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76844-107">*pwszmruregkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76844-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76844-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="76844-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="76844-109">Ein Zeiger auf einen Puffer, der den Registrierungsschlüssel enthält, der die Zeichen folgen für die MRU-Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="76844-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="76844-110">*dwMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76844-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76844-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="76844-111">Type: **DWORD**</span></span>

<span data-ttu-id="76844-112">Die maximale Anzahl von Einträgen, die von *pwszmruregkey* entnommen werden können.</span><span class="sxs-lookup"><span data-stu-id="76844-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76844-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76844-113">Return value</span></span>

<span data-ttu-id="76844-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="76844-114">Type: **HRESULT**</span></span>

<span data-ttu-id="76844-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="76844-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76844-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76844-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="76844-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="76844-117">Requirements</span></span>



| <span data-ttu-id="76844-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76844-118">Requirement</span></span> | <span data-ttu-id="76844-119">Wert</span><span class="sxs-lookup"><span data-stu-id="76844-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76844-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76844-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76844-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76844-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="76844-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76844-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76844-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76844-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




