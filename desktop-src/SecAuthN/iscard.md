---
description: Ermöglicht das Öffnen und Verwalten einer Verbindung mit einer Smartcard.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Iscard-Schnittstelle (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528151"
---
# <a name="iscard-interface"></a><span data-ttu-id="9b177-103">Iscard-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9b177-103">ISCard interface</span></span>

<span data-ttu-id="9b177-104">\[Die **iscard** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b177-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9b177-105">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9b177-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9b177-106">Mit der **iscard** -Schnittstelle können Sie eine Verbindung zu einer [*Smartcard*](../secgloss/s-gly.md)öffnen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="9b177-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="9b177-107">Für jede Verbindung mit einer Karte ist eine einzelne, entsprechende Instanz der **iscard** -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b177-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="9b177-108">Der Smartcard- [*Ressourcen-Manager*](../secgloss/r-gly.md) muss immer verfügbar sein, wenn eine Instanz von **iscard** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9b177-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="9b177-109">Wenn dieser Dienst nicht verfügbar ist, tritt bei der Erstellung der-Schnittstelle ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="9b177-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="9b177-110">Das folgende Beispiel zeigt eine typische Verwendung der **iscard** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b177-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="9b177-111">Die **iscard** -Schnittstelle wird verwendet, um eine Verbindung mit der Smartcard herzustellen, eine [*Transaktion*](../secgloss/t-gly.md)zu senden und die Smartcard freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9b177-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="9b177-112">**So übermitteln Sie eine Transaktion an eine bestimmte Karte**</span><span class="sxs-lookup"><span data-stu-id="9b177-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="9b177-113">Erstellen Sie eine **iscard** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b177-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="9b177-114">Fügen Sie an eine Smartcard an, indem Sie einen [*Smartcardleser*](../secgloss/r-gly.md) oder ein zuvor ermitteltes, gültiges Handle angeben.</span><span class="sxs-lookup"><span data-stu-id="9b177-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="9b177-115">Erstellen Sie Transaktions Befehle mit [**iscardcmd**](iscardcmd.md)-und [**ISCardISO7816**](iscardiso7816.md) -smartcardschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9b177-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="9b177-116">Verwenden Sie **iscard** , um die Transaktions Befehle zur Verarbeitung durch die Smartcard zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9b177-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="9b177-117">Verwenden Sie **iscard** , um die Smartcard freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9b177-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="9b177-118">Geben Sie die **iscard** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="9b177-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9b177-119">Member</span><span class="sxs-lookup"><span data-stu-id="9b177-119">Members</span></span>

<span data-ttu-id="9b177-120">Die **iscard** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b177-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9b177-121">Die **iscard** verfügt auch über die folgenden Arten von Mitgliedern:</span><span class="sxs-lookup"><span data-stu-id="9b177-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="9b177-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="9b177-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b177-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b177-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b177-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="9b177-124">Methods</span></span>

<span data-ttu-id="9b177-125">Die **iscard** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9b177-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="9b177-126">Methode</span><span class="sxs-lookup"><span data-stu-id="9b177-126">Method</span></span>                                          | <span data-ttu-id="9b177-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b177-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b177-128">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="9b177-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="9b177-129">Fügt ein-Objekt an ein geöffnetes und konfiguriertes smartcardhandle an.</span><span class="sxs-lookup"><span data-stu-id="9b177-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="9b177-130">**Attachbyreader**</span><span class="sxs-lookup"><span data-stu-id="9b177-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="9b177-131">Öffnet die Smartcard im benannten Reader.</span><span class="sxs-lookup"><span data-stu-id="9b177-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="9b177-132">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="9b177-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="9b177-133">Schließt die geöffnete Verbindung mit der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="9b177-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="9b177-134">**Sperrkarte**</span><span class="sxs-lookup"><span data-stu-id="9b177-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="9b177-135">Anspruchs exklusiver Zugriff auf die Smartcard.</span><span class="sxs-lookup"><span data-stu-id="9b177-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="9b177-136">**Erneut**</span><span class="sxs-lookup"><span data-stu-id="9b177-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="9b177-137">Setzt die Smartcard zurück und initialisiert sie erneut.</span><span class="sxs-lookup"><span data-stu-id="9b177-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="9b177-138">**Transaktion**</span><span class="sxs-lookup"><span data-stu-id="9b177-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="9b177-139">Führt einen Schreib-und Lesevorgang für den smartcardbefehl ([*Application Protocol Data Unit*](../secgloss/a-gly.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="9b177-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="9b177-140">**Unlockcard**</span><span class="sxs-lookup"><span data-stu-id="9b177-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="9b177-141">Gibt exklusiven Zugriff auf die Smartcard frei.</span><span class="sxs-lookup"><span data-stu-id="9b177-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="9b177-142">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b177-142">Properties</span></span>

<span data-ttu-id="9b177-143">Die **iscard** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b177-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="9b177-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9b177-144">Property</span></span>                                               | <span data-ttu-id="9b177-145">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="9b177-145">Access type</span></span>          | <span data-ttu-id="9b177-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b177-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b177-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="9b177-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="9b177-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b177-148">Read-only</span></span><br/> | <span data-ttu-id="9b177-149">Ruft die [*ATR-Zeichenfolge*](../secgloss/a-gly.md) der Smartcard ab.</span><span class="sxs-lookup"><span data-stu-id="9b177-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="9b177-150">**Cardhandle**</span><span class="sxs-lookup"><span data-stu-id="9b177-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="9b177-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b177-151">Read-only</span></span><br/> | <span data-ttu-id="9b177-152">Ruft das Handle für die verbundene Smartcard ab.</span><span class="sxs-lookup"><span data-stu-id="9b177-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="9b177-153">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="9b177-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="9b177-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b177-154">Read-only</span></span><br/> | <span data-ttu-id="9b177-155">Ruft das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle ab.</span><span class="sxs-lookup"><span data-stu-id="9b177-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="9b177-156">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="9b177-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="9b177-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b177-157">Read-only</span></span><br/> | <span data-ttu-id="9b177-158">Ruft den Bezeichner des zurzeit auf der Smartcard verwendeten Protokolls ab.</span><span class="sxs-lookup"><span data-stu-id="9b177-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="9b177-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b177-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="9b177-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b177-160">Read-only</span></span><br/> | <span data-ttu-id="9b177-161">Ruft den aktuellen [*Zustand*](../secgloss/s-gly.md) der [*Smartcard*](../secgloss/s-gly.md) ab.</span><span class="sxs-lookup"><span data-stu-id="9b177-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b177-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b177-162">Requirements</span></span>



| <span data-ttu-id="9b177-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b177-163">Requirement</span></span> | <span data-ttu-id="9b177-164">Wert</span><span class="sxs-lookup"><span data-stu-id="9b177-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b177-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b177-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9b177-166">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b177-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b177-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b177-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9b177-168">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b177-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b177-169">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9b177-169">End of client support</span></span><br/>    | <span data-ttu-id="9b177-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b177-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9b177-171">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9b177-171">End of server support</span></span><br/>    | <span data-ttu-id="9b177-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b177-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9b177-173">Header</span><span class="sxs-lookup"><span data-stu-id="9b177-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b177-174"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9b177-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b177-175">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b177-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b177-176"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b177-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b177-177">DLL</span><span class="sxs-lookup"><span data-stu-id="9b177-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b177-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b177-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b177-179">IID</span><span class="sxs-lookup"><span data-stu-id="9b177-179">IID</span></span><br/>                      | <span data-ttu-id="9b177-180">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="9b177-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
