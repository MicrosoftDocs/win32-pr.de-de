---
title: Session-Objekt (WSManDisp. h)
description: Definiert Vorgänge und Sitzungs Einstellungen.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Sitzungs Objekt Windows-Remoteverwaltung
- Sitzungs Objekt Windows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957220"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="bb1b1-105">Session-Objekt (WSManDisp. h)</span><span class="sxs-lookup"><span data-stu-id="bb1b1-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="bb1b1-106">Definiert Vorgänge und Sitzungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-106">Defines operations and session settings.</span></span> <span data-ttu-id="bb1b1-107">Alle Windows-Remoteverwaltung Vorgänge erfordern das Erstellen einer **Sitzung** , die eine Verbindung mit einem Remote Computer, einem [*Base Management Controller*](windows-remote-management-glossary.md) (BMC) oder dem lokalen Computer herstellt.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="bb1b1-108">WinRM-Netzwerk Vorgänge umfassen das aufrufen, schreiben, Auflisten von Daten oder das Aufrufen von Methoden.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="bb1b1-109">Die Methoden des **Session** -Objekts spiegeln die grundlegenden Vorgänge wider, die im WS-Management-Protokoll definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="bb1b1-110">Member</span><span class="sxs-lookup"><span data-stu-id="bb1b1-110">Members</span></span>

<span data-ttu-id="bb1b1-111">Das **Sitzungs** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bb1b1-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="bb1b1-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="bb1b1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb1b1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb1b1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb1b1-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="bb1b1-114">Methods</span></span>

<span data-ttu-id="bb1b1-115">Das **Sitzungs** Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="bb1b1-116">Methode</span><span class="sxs-lookup"><span data-stu-id="bb1b1-116">Method</span></span>                                 | <span data-ttu-id="bb1b1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb1b1-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb1b1-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="bb1b1-119">Erstellt eine neue Instanz einer Ressource und gibt den URI des neuen-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="bb1b1-120">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="bb1b1-121">Löscht die im Ressourcen-URI angegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="bb1b1-122">**Aufzählen**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="bb1b1-123">Listet eine Auflistung, eine Tabelle oder eine Nachrichtenprotokoll Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="bb1b1-124">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="bb1b1-125">Ruft eine Ressource vom Dienst ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="bb1b1-126">**Identifizieren**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="bb1b1-127">Fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="bb1b1-128">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="bb1b1-129">Ruft eine Methode auf, die die Ergebnisse des Methoden Aufrufes zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="bb1b1-130">**Stellte**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="bb1b1-131">Aktualisieren Sie eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="bb1b1-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb1b1-132">Properties</span></span>

<span data-ttu-id="bb1b1-133">Das **Sitzungs** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="bb1b1-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb1b1-134">Property</span></span>                                            | <span data-ttu-id="bb1b1-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="bb1b1-135">Access type</span></span>           | <span data-ttu-id="bb1b1-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb1b1-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb1b1-137">**Batchitems**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="bb1b1-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb1b1-138">Read/write</span></span><br/> | <span data-ttu-id="bb1b1-139">Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="bb1b1-140">Dieser Wert kann während einer Enumeration nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="bb1b1-141">Standardmäßig ist der Standardwert eine unbegrenzte Anzahl von Elementen.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="bb1b1-142">Der Ressourcenanbieter kann ein Limit festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="bb1b1-143">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="bb1b1-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bb1b1-144">Read-only</span></span><br/>  | <span data-ttu-id="bb1b1-145">Ruft zusätzliche Fehlerinformationen in einem XML-Stream ab.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="bb1b1-146">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="bb1b1-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="bb1b1-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb1b1-147">Read/write</span></span><br/> | <span data-ttu-id="bb1b1-148">Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="bb1b1-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb1b1-149">Remarks</span></span>

<span data-ttu-id="bb1b1-150">Das **Sitzungs** Objekt entspricht der [**iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="bb1b1-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb1b1-151">Examples</span></span>

<span data-ttu-id="bb1b1-152">Im folgenden VBScript-Codebeispiel wird gezeigt, wie ein **Sitzungs** Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb1b1-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="bb1b1-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb1b1-153">Requirements</span></span>



| <span data-ttu-id="bb1b1-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb1b1-154">Requirement</span></span> | <span data-ttu-id="bb1b1-155">Wert</span><span class="sxs-lookup"><span data-stu-id="bb1b1-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1b1-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb1b1-156">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1b1-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb1b1-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bb1b1-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb1b1-158">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1b1-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb1b1-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bb1b1-160">Header</span><span class="sxs-lookup"><span data-stu-id="bb1b1-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb1b1-161"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b1-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb1b1-162">IDL</span><span class="sxs-lookup"><span data-stu-id="bb1b1-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb1b1-163"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b1-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bb1b1-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb1b1-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb1b1-165"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b1-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb1b1-166">DLL</span><span class="sxs-lookup"><span data-stu-id="bb1b1-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb1b1-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b1-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb1b1-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb1b1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1b1-169">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="bb1b1-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="bb1b1-170">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="bb1b1-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="bb1b1-171">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="bb1b1-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="bb1b1-172">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="bb1b1-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="bb1b1-173">Abrufen von Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="bb1b1-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="bb1b1-174">Abrufen von Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="bb1b1-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





