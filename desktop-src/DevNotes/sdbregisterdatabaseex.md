---
description: Registriert die angegebene Datenbank.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Sdbregisterdatabaseex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523344"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="7e16b-103">Sdbregisterdatabaseex-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e16b-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="7e16b-104">Registriert die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e16b-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e16b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e16b-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="7e16b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e16b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e16b-107">*pszdatabasepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e16b-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e16b-108">Der Daten Bank Pfad.</span><span class="sxs-lookup"><span data-stu-id="7e16b-108">The database path.</span></span> <span data-ttu-id="7e16b-109">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7e16b-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7e16b-110">*dwdatabasetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e16b-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e16b-111">Der Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="7e16b-111">The database type.</span></span> <span data-ttu-id="7e16b-112">Eine Liste der Werte finden Sie unter [Shim-Datenbanktypen](shim-database-types.md) .</span><span class="sxs-lookup"><span data-stu-id="7e16b-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="7e16b-113">*ptimestamp* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7e16b-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e16b-114">Der Zeitstempel für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e16b-114">The time stamp for the database.</span></span> <span data-ttu-id="7e16b-115">Wenn dieser Parameter **null** ist, wird die Systemzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e16b-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e16b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e16b-116">Return value</span></span>

<span data-ttu-id="7e16b-117">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="7e16b-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e16b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e16b-118">Remarks</span></span>

<span data-ttu-id="7e16b-119">Eine Datenbank muss registriert werden, bevor Sie andere SDB-Funktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7e16b-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e16b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e16b-120">Requirements</span></span>



| <span data-ttu-id="7e16b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e16b-121">Requirement</span></span> | <span data-ttu-id="7e16b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7e16b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e16b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e16b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7e16b-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e16b-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7e16b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e16b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7e16b-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e16b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e16b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7e16b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e16b-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e16b-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e16b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e16b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e16b-130">**Sdbunregisterdatabase**</span><span class="sxs-lookup"><span data-stu-id="7e16b-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




