---
description: Öffnet die angegebene AppHelp-Detail Datenbank.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Sdbopenapphelpdetailsdatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125623"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="fbc5f-103">Sdbopenapphelpdetailsdatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbc5f-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="fbc5f-104">Öffnet die angegebene AppHelp-Detail Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc5f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbc5f-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="fbc5f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc5f-107">*pwsdetailsdatabasepath* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="fbc5f-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc5f-108">Der Daten Bank Pfad.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-108">The database path.</span></span> <span data-ttu-id="fbc5f-109">Wenn dieser Parameter **null** ist, wird die lokale Systemdatenbank geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc5f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbc5f-110">Return value</span></span>

<span data-ttu-id="fbc5f-111">Die-Funktion gibt ein Handle für die AppHelp-Detail Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc5f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbc5f-112">Requirements</span></span>



| <span data-ttu-id="fbc5f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbc5f-113">Requirement</span></span> | <span data-ttu-id="fbc5f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fbc5f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc5f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbc5f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc5f-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbc5f-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fbc5f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbc5f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc5f-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbc5f-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fbc5f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fbc5f-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc5f-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbc5f-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




