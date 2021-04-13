---
description: Hebt die Registrierung der angegebenen Datenbank auf, sodass Sie nicht mehr verfügbar ist.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Sdbunregisterdatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483118"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="3e41c-103">Sdbunregisterdatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e41c-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="3e41c-104">Hebt die Registrierung der angegebenen Datenbank auf, sodass Sie nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3e41c-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e41c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e41c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="3e41c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e41c-107">*pguiddb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e41c-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e41c-108">Die GUID der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3e41c-108">The GUID of the database.</span></span> <span data-ttu-id="3e41c-109">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3e41c-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e41c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e41c-110">Return value</span></span>

<span data-ttu-id="3e41c-111">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="3e41c-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e41c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e41c-112">Requirements</span></span>



| <span data-ttu-id="3e41c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e41c-113">Requirement</span></span> | <span data-ttu-id="3e41c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3e41c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e41c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e41c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e41c-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e41c-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e41c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e41c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e41c-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e41c-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3e41c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3e41c-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e41c-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e41c-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e41c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e41c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e41c-122">**Sdbregisterdatabaseex**</span><span class="sxs-lookup"><span data-stu-id="3e41c-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




