---
description: Die iscardlocate-Schnittstelle stellt Dienste für die Suche nach einer Smartcard anhand ihres Namens bereit.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Iscardlocate-Schnittstelle (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368825"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="9ead7-103">Iscardlocate-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ead7-103">ISCardLocate interface</span></span>

<span data-ttu-id="9ead7-104">\[Die **iscardlocate** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9ead7-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ead7-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ead7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ead7-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9ead7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9ead7-107">Die **iscardlocate** -Schnittstelle stellt Dienste für die Suche nach einer [*Smartcard*](../secgloss/s-gly.md) anhand ihres Namens bereit.</span><span class="sxs-lookup"><span data-stu-id="9ead7-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="9ead7-108">Diese Schnittstelle kann die Smartcard- [*Benutzeroberfläche*](../secgloss/u-gly.md) anzeigen, wenn Sie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9ead7-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="9ead7-109">Das folgende Szenario zeigt eine typische Verwendung der **iscardlocate** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9ead7-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="9ead7-110">Die **iscardlocate** -Schnittstelle wird verwendet, um eine [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (APDU) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ead7-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="9ead7-111">**So suchen Sie eine bestimmte Karte mithilfe Ihres Namens**</span><span class="sxs-lookup"><span data-stu-id="9ead7-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="9ead7-112">Erstellen Sie eine **iscardlocate** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9ead7-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="9ead7-113">Wenn Sie den Namen "konfigurierter Smartcard" verwenden möchten, müssen Sie " [**konfigurierter**](iscardlocate-configurecardnamesearch.md) Name" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9ead7-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="9ead7-114">Ruft [**findcard**](iscardlocate-findcard.md) auf, um nach der Smartcard zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9ead7-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="9ead7-115">Interpretieren der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9ead7-115">Interpret the results.</span></span>
5.  <span data-ttu-id="9ead7-116">Geben Sie die **iscardlocate** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="9ead7-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9ead7-117">Member</span><span class="sxs-lookup"><span data-stu-id="9ead7-117">Members</span></span>

<span data-ttu-id="9ead7-118">Die **iscardlocate** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9ead7-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9ead7-119">**Iscardlocate** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9ead7-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="9ead7-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="9ead7-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ead7-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="9ead7-121">Methods</span></span>

<span data-ttu-id="9ead7-122">Die **iscardlocate** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9ead7-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="9ead7-123">Methode</span><span class="sxs-lookup"><span data-stu-id="9ead7-123">Method</span></span>                                                                  | <span data-ttu-id="9ead7-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ead7-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="9ead7-125">**Konfigurieren von "Konfigurations-guidsearch"**</span><span class="sxs-lookup"><span data-stu-id="9ead7-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="9ead7-126">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9ead7-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="9ead7-127">**Konfigurieren von "Konfigurations namesearch"**</span><span class="sxs-lookup"><span data-stu-id="9ead7-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="9ead7-128">Gibt den Namen der Karte an, die bei der Suche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ead7-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="9ead7-129">**Findcard**</span><span class="sxs-lookup"><span data-stu-id="9ead7-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="9ead7-130">Sucht nach der Smartcard und öffnet eine gültige Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9ead7-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ead7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ead7-131">Requirements</span></span>



| <span data-ttu-id="9ead7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ead7-132">Requirement</span></span> | <span data-ttu-id="9ead7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9ead7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ead7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ead7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9ead7-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ead7-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ead7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ead7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9ead7-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ead7-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ead7-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9ead7-138">End of client support</span></span><br/>    | <span data-ttu-id="9ead7-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ead7-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9ead7-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9ead7-140">End of server support</span></span><br/>    | <span data-ttu-id="9ead7-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ead7-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9ead7-142">Header</span><span class="sxs-lookup"><span data-stu-id="9ead7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ead7-143"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9ead7-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ead7-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ead7-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ead7-145"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ead7-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ead7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9ead7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ead7-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ead7-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ead7-148">IID</span><span class="sxs-lookup"><span data-stu-id="9ead7-148">IID</span></span><br/>                      | <span data-ttu-id="9ead7-149">IID \_ iscardlocate ist als 1461aacd-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="9ead7-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
