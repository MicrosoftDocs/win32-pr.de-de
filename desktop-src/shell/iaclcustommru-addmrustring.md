---
description: Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.
title: 'Iaclcustommru:: addmrustring-Methode'
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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994638"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="f81b1-103">Iaclcustommru:: addmrustring-Methode</span><span class="sxs-lookup"><span data-stu-id="f81b1-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="f81b1-104">Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="f81b1-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f81b1-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="f81b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f81b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81b1-107">*pwszentry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f81b1-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81b1-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f81b1-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="f81b1-109">Ein Zeiger auf einen Puffer, der den neuen Eintrag enthält.</span><span class="sxs-lookup"><span data-stu-id="f81b1-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81b1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f81b1-110">Return value</span></span>

<span data-ttu-id="f81b1-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f81b1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f81b1-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f81b1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f81b1-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f81b1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81b1-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f81b1-114">Requirements</span></span>



| <span data-ttu-id="f81b1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f81b1-115">Requirement</span></span> | <span data-ttu-id="f81b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f81b1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f81b1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f81b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f81b1-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f81b1-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f81b1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f81b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f81b1-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f81b1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




