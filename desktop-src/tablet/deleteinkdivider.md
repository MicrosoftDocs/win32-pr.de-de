---
description: Löscht ein InkDivider-Objekt und gibt die zugeordneten Ressourcen frei.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: Delta-einkdivider-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867735"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="15721-103">Delta-einkdivider-Funktion</span><span class="sxs-lookup"><span data-stu-id="15721-103">DeleteInkDivider function</span></span>

<span data-ttu-id="15721-104">Löscht ein [**InkDivider**](inkdivider-class.md) -Objekt und gibt die zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="15721-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="15721-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="15721-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="15721-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="15721-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="15721-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="15721-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15721-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15721-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15721-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="15721-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15721-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15721-110">Return value</span></span>

<span data-ttu-id="15721-111">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="15721-111">This function can return one of these values.</span></span>



| <span data-ttu-id="15721-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="15721-112">Return code</span></span>                                                                                  | <span data-ttu-id="15721-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15721-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="15721-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15721-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="15721-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15721-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="15721-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="15721-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="15721-117">Der *hdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="15721-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15721-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15721-118">Requirements</span></span>



| <span data-ttu-id="15721-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15721-119">Requirement</span></span> | <span data-ttu-id="15721-120">Wert</span><span class="sxs-lookup"><span data-stu-id="15721-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15721-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15721-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15721-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15721-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="15721-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15721-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15721-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15721-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="15721-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15721-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="15721-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15721-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




