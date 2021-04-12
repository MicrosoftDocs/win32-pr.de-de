---
description: Definiert Methoden, die die iTablet-Schnittstellen Ereignisse verarbeiten.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Itableteventsink-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218367"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="f319f-103">Itableteventsink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f319f-103">ITabletEventSink interface</span></span>

<span data-ttu-id="f319f-104">Definiert Methoden, die die [**iTablet-Schnittstellen**](itablet.md) Ereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f319f-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="f319f-105">Member</span><span class="sxs-lookup"><span data-stu-id="f319f-105">Members</span></span>

<span data-ttu-id="f319f-106">Die **itableteventsink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f319f-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f319f-107">**Itableteventsink** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f319f-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="f319f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f319f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f319f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f319f-109">Methods</span></span>

<span data-ttu-id="f319f-110">Die **itableteventsink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f319f-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="f319f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f319f-111">Method</span></span>                                                        | <span data-ttu-id="f319f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f319f-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f319f-113">**Contextcreate**</span><span class="sxs-lookup"><span data-stu-id="f319f-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="f319f-114">Tritt auf, wenn ein neuer Tablet-Kontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f319f-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="f319f-115">**Contextdestroy**</span><span class="sxs-lookup"><span data-stu-id="f319f-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="f319f-116">Tritt auf, wenn ein Tablet-Kontext zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="f319f-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="f319f-117">**Cursor**</span><span class="sxs-lookup"><span data-stu-id="f319f-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="f319f-118">Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="f319f-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="f319f-119">**Cursor Bereich**</span><span class="sxs-lookup"><span data-stu-id="f319f-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="f319f-120">Tritt auf, wenn ein Tablettstift in den Bereich der Erkennung des Digitalisierungsprogramms kommt.</span><span class="sxs-lookup"><span data-stu-id="f319f-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="f319f-121">**Cursor verschieben**</span><span class="sxs-lookup"><span data-stu-id="f319f-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="f319f-122">Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f319f-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="f319f-123">**Currsornew**</span><span class="sxs-lookup"><span data-stu-id="f319f-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="f319f-124">Tritt auf, wenn dem System ein neuer Tablettstift hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f319f-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="f319f-125">**Cursor-Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="f319f-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="f319f-126">Tritt auf, wenn der Tablettstift den physischen Erkennungsbereich (Nähe) des Tablets verlässt.</span><span class="sxs-lookup"><span data-stu-id="f319f-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="f319f-127">**Cursor**</span><span class="sxs-lookup"><span data-stu-id="f319f-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="f319f-128">Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="f319f-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="f319f-129">**Pakete**</span><span class="sxs-lookup"><span data-stu-id="f319f-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="f319f-130">Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.</span><span class="sxs-lookup"><span data-stu-id="f319f-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="f319f-131">**System Event**</span><span class="sxs-lookup"><span data-stu-id="f319f-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="f319f-132">Tritt auf, wenn ein System Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f319f-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="f319f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f319f-133">Remarks</span></span>

<span data-ttu-id="f319f-134">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="f319f-134">Developers should not use this interface.</span></span>

<span data-ttu-id="f319f-135">Der folgende Code zeigt, wie die **itableteventsink** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f319f-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="f319f-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f319f-136">Requirements</span></span>



| <span data-ttu-id="f319f-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f319f-137">Requirement</span></span> | <span data-ttu-id="f319f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f319f-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f319f-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f319f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f319f-140">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f319f-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f319f-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f319f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f319f-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f319f-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f319f-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f319f-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f319f-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f319f-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

