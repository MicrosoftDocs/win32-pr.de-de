---
description: Erstellt einen Schlüssel aus einer Zeichenfolge.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Sdbmakeindexkeyfromstring-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958119"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="1d4b5-103">Sdbmakeindexkeyfromstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d4b5-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="1d4b5-104">Erstellt einen Schlüssel aus einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d4b5-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d4b5-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="1d4b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4b5-107">*pwszkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d4b5-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4b5-108">Die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d4b5-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4b5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d4b5-109">Return value</span></span>

<span data-ttu-id="1d4b5-110">Die-Funktion gibt den Schlüssel zurück, oder 0, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="1d4b5-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4b5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d4b5-111">Remarks</span></span>

<span data-ttu-id="1d4b5-112">Der Standard Index Schlüssel ist die ersten acht Zeichen der Zeichenfolge, die in Großbuchstaben konvertiert und dann in einen **ULONGLONG** -Wert umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="1d4b5-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4b5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4b5-113">Requirements</span></span>



| <span data-ttu-id="1d4b5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d4b5-114">Requirement</span></span> | <span data-ttu-id="1d4b5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4b5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4b5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d4b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4b5-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4b5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1d4b5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d4b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4b5-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4b5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1d4b5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4b5-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4b5-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b5-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




