---
title: Rtmblockdeleteroutes-Funktion (RTM. h)
description: Die rtmblockdeleteroutes-Funktion löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Rtmblockdeleteroutes-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477511"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="4189f-104">Rtmblockdeleteroutes-Funktion</span><span class="sxs-lookup"><span data-stu-id="4189f-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="4189f-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4189f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="4189f-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="4189f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="4189f-107">Die **rtmblockdeleteroutes** -Funktion löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4189f-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="4189f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4189f-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="4189f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4189f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4189f-110">*Clienthandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4189f-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4189f-111">Handle, das den Client und somit das Routing Protokoll der zu löschenden Routen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4189f-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4189f-112">*Enumerationflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4189f-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4189f-113">Gibt an, welche Routen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4189f-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="4189f-114">Mit diesem Parameter wird der Satz gelöschter Routen auf eine Teilmenge beschränkt, die durch die folgenden Flags definiert ist, sowie auf die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterienparameter* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4189f-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="4189f-115">Die Flags sind identisch mit denen, die in [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md) verwendet werden, mit dem Unterschied, dass RTM \_ \_ \_ für **rtmblockdeleteroutes** nur die besten Routen redundant ist.</span><span class="sxs-lookup"><span data-stu-id="4189f-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="4189f-116">Die beste Routen Bezeichnung wird angepasst, wenn Routen gelöscht werden, sodass die Funktion schließlich alle Routen in der Teilmenge löscht.</span><span class="sxs-lookup"><span data-stu-id="4189f-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="4189f-117">*Kriterien* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4189f-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4189f-118">Zeiger auf eine Protokoll familienspezifische Routen Struktur ( [**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="4189f-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="4189f-119">Die Element Werte in dieser Struktur entsprechen den Flags, die durch den *enumerationflags* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4189f-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4189f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4189f-120">Return value</span></span>

<span data-ttu-id="4189f-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="4189f-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="4189f-122">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="4189f-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="4189f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4189f-123">Value</span></span>                                                                                                       | <span data-ttu-id="4189f-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4189f-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4189f-125"><dt>**Fehler \_ ohne \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="4189f-126">Es sind keine Routen vorhanden, die die angegebenen Kriterien aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4189f-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="4189f-127"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="4189f-128">Der *Clienthandle* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4189f-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="4189f-129"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="4189f-130">Mindestens ein Eingabeparameter ist ungültig, z. b. sind die Enumerationsflags ungültig.</span><span class="sxs-lookup"><span data-stu-id="4189f-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="4189f-131"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="4189f-132">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4189f-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4189f-133"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="4189f-134">Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4189f-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="4189f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4189f-135">Remarks</span></span>

<span data-ttu-id="4189f-136">Die Funktion generiert geeignete Benachrichtigungs Meldungen für alle registrierten Clients, einschließlich des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="4189f-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="4189f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4189f-137">Requirements</span></span>



| <span data-ttu-id="4189f-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4189f-138">Requirement</span></span> | <span data-ttu-id="4189f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="4189f-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4189f-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4189f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4189f-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4189f-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4189f-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4189f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4189f-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4189f-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4189f-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4189f-144">End of server support</span></span><br/>    | <span data-ttu-id="4189f-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4189f-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="4189f-146">Header</span><span class="sxs-lookup"><span data-stu-id="4189f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4189f-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="4189f-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4189f-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="4189f-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="4189f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="4189f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4189f-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4189f-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4189f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4189f-153">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="4189f-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="4189f-154">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="4189f-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="4189f-155">**Rtmkreateenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="4189f-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="4189f-156">**Rtmregisterclient**</span><span class="sxs-lookup"><span data-stu-id="4189f-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





