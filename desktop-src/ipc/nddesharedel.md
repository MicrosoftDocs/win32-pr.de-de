---
description: Löscht eine DDE-Freigabe aus dem DDE-Freigabe Datenbank-Manager (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Nddebug-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346675"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="7c9fe-103">Nddebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c9fe-103">NDdeShareDel function</span></span>

<span data-ttu-id="7c9fe-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="7c9fe-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="7c9fe-106">Löscht eine DDE-Freigabe aus dem DDE-Freigabe Datenbank-Manager (DSDM).</span><span class="sxs-lookup"><span data-stu-id="7c9fe-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c9fe-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="7c9fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c9fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9fe-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c9fe-110">Der Name des Servers, dessen DSDM geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="7c9fe-111">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c9fe-112">Der Name der Freigabe, die aus der DSDM gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="7c9fe-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c9fe-114">*wReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c9fe-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-115">Reserved.</span></span> <span data-ttu-id="7c9fe-116">Dieser Parameter muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9fe-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c9fe-117">Return value</span></span>

<span data-ttu-id="7c9fe-118">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="7c9fe-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="7c9fe-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9fe-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c9fe-120">Remarks</span></span>

<span data-ttu-id="7c9fe-121">Um eine DDE-Freigabe aus der DSDM zu löschen, müssen Sie über die entsprechenden Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7c9fe-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="7c9fe-122">Der Freigabe Ersteller verfügt über die Berechtigung "Löschen".</span><span class="sxs-lookup"><span data-stu-id="7c9fe-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9fe-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c9fe-123">Requirements</span></span>



| <span data-ttu-id="7c9fe-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c9fe-124">Requirement</span></span> | <span data-ttu-id="7c9fe-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7c9fe-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9fe-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c9fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9fe-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c9fe-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c9fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9fe-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c9fe-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7c9fe-130">Header</span><span class="sxs-lookup"><span data-stu-id="7c9fe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9fe-131"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9fe-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c9fe-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c9fe-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c9fe-133"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c9fe-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c9fe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7c9fe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c9fe-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c9fe-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c9fe-136">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="7c9fe-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c9fe-137">**Nddeaktiviert** (Unicode) und **nddebug** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c9fe-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="7c9fe-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c9fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9fe-139">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="7c9fe-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="7c9fe-140">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7c9fe-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




