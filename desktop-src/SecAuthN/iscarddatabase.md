---
description: Die iscarddatabase-Schnittstelle stellt die Methoden zum Ausführen der Daten Bank Vorgänge des Smartcard-Ressourcen-Managers bereit.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Iscarddatabase-Schnittstelle (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372827"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="3803c-103">Iscarddatabase-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3803c-103">ISCardDatabase interface</span></span>

<span data-ttu-id="3803c-104">\[Die **iscarddatabase** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3803c-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3803c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3803c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3803c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3803c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3803c-107">Die **iscarddatabase** -Schnittstelle stellt die Methoden zum Ausführen der Daten Bank Vorgänge des [*Smartcard*](../secgloss/s-gly.md) [*-Ressourcen-Managers*](../secgloss/r-gly.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="3803c-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="3803c-108">Zu diesen Vorgängen gehören das Auflisten bekannter Smartcards, [*Leser*](../secgloss/r-gly.md)und Lesergruppen sowie das Abrufen der Schnittstellen, die von einer Smartcard und Ihrem [*primären Dienstanbieter*](../secgloss/p-gly.md)unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3803c-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="3803c-109">Der Bezeichner des primären Dienstanbieters ist eine com-GUID, die zum Instanziieren und Verwenden der COM-Objekte für eine bestimmte Karte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3803c-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="3803c-110">Das folgende Beispiel zeigt eine typische Verwendung der **iscarddatabase** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3803c-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="3803c-111">In diesem Fall wird die **iscarddatabase** -Schnittstelle verwendet, um alle bekannten Smartcards aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="3803c-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="3803c-112">**So übermitteln Sie eine Transaktion an eine bestimmte Karte**</span><span class="sxs-lookup"><span data-stu-id="3803c-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="3803c-113">Erstellen Sie eine **iscarddatabase** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3803c-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="3803c-114">Rufen Sie [**listcards**](iscarddatabase-listcards.md) auf, um alle bekannten Smartcards auf der Grundlage einer [*ATR-Zeichenfolge*](../secgloss/a-gly.md) oder ihrer unterstützten Schnittstellen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3803c-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="3803c-115">Geben Sie die **iscarddatabase** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="3803c-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="3803c-116">Member</span><span class="sxs-lookup"><span data-stu-id="3803c-116">Members</span></span>

<span data-ttu-id="3803c-117">Die **iscarddatabase** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3803c-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3803c-118">**Iscarddatabase** verfügt auch über die folgenden Typen von Mitgliedern:</span><span class="sxs-lookup"><span data-stu-id="3803c-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="3803c-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="3803c-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3803c-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="3803c-120">Methods</span></span>

<span data-ttu-id="3803c-121">Die **iscarddatabase** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3803c-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="3803c-122">Methode</span><span class="sxs-lookup"><span data-stu-id="3803c-122">Method</span></span>                                                          | <span data-ttu-id="3803c-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3803c-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3803c-124">**Getprovidercardid**</span><span class="sxs-lookup"><span data-stu-id="3803c-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="3803c-125">Ruft den Bezeichner des [*primären Dienstanbieters*](../secgloss/p-gly.md) für eine bestimmte Smartcard ab.</span><span class="sxs-lookup"><span data-stu-id="3803c-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="3803c-126">**Listcardinterfaces**</span><span class="sxs-lookup"><span data-stu-id="3803c-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="3803c-127">Ruft die Schnittstellen Bezeichner (GUIDs) aller Schnittstellen ab, die von einer bestimmten Smartcard unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3803c-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="3803c-128">**Listcards**</span><span class="sxs-lookup"><span data-stu-id="3803c-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="3803c-129">Ruft alle smartcardnamen ab, die einem bestimmten Satz von Schnittstellen Bezeichnerzeichen (GUIDs) oder einer [*ATR-Zeichenfolge*](../secgloss/a-gly.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3803c-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="3803c-130">**Listreadergroups**</span><span class="sxs-lookup"><span data-stu-id="3803c-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="3803c-131">Ruft die Namen der [*Lesergruppen*](../secgloss/r-gly.md) ab, die dem Ressourcen-Manager bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="3803c-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="3803c-132">**Listreaders**</span><span class="sxs-lookup"><span data-stu-id="3803c-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="3803c-133">Rufen Sie die Namen der [*Leser*](../secgloss/r-gly.md) ab, von denen der Ressourcen-Manager wissen hat.</span><span class="sxs-lookup"><span data-stu-id="3803c-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="3803c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3803c-134">Requirements</span></span>



| <span data-ttu-id="3803c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3803c-135">Requirement</span></span> | <span data-ttu-id="3803c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="3803c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3803c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3803c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3803c-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3803c-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3803c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3803c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3803c-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3803c-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3803c-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3803c-141">End of client support</span></span><br/>    | <span data-ttu-id="3803c-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3803c-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3803c-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3803c-143">End of server support</span></span><br/>    | <span data-ttu-id="3803c-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3803c-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3803c-145">Header</span><span class="sxs-lookup"><span data-stu-id="3803c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3803c-146"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3803c-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3803c-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3803c-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="3803c-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3803c-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3803c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3803c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3803c-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3803c-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3803c-151">IID</span><span class="sxs-lookup"><span data-stu-id="3803c-151">IID</span></span><br/>                      | <span data-ttu-id="3803c-152">IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="3803c-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
