---
description: Gibt die angegebenen Datei Attributdaten frei.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Sdbfrefileattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747688"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="607a0-103">Sdbfrefileattribute-Funktion</span><span class="sxs-lookup"><span data-stu-id="607a0-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="607a0-104">Gibt die angegebenen Datei Attributdaten frei.</span><span class="sxs-lookup"><span data-stu-id="607a0-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="607a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="607a0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="607a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="607a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607a0-107">*pfileattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="607a0-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607a0-108">Eine [**attrinfo**](attrinfo.md) -Struktur, die von der [**sdbgetfileattribute**](sdbgetfileattributes.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="607a0-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607a0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="607a0-109">Return value</span></span>

<span data-ttu-id="607a0-110">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="607a0-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="607a0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="607a0-111">Requirements</span></span>



| <span data-ttu-id="607a0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="607a0-112">Requirement</span></span> | <span data-ttu-id="607a0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="607a0-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="607a0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="607a0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="607a0-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="607a0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="607a0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="607a0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="607a0-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="607a0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="607a0-118">DLL</span><span class="sxs-lookup"><span data-stu-id="607a0-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="607a0-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="607a0-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607a0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="607a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607a0-121">**Sdbgetfileattribute**</span><span class="sxs-lookup"><span data-stu-id="607a0-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




