---
description: Die übergeordnete Klasse, von der alle System Ereignis-Ablauf Verfolgungs Klassen abgeleitet werden. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977817"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="c981f-104">MSNT \_ systemtrace-Klasse</span><span class="sxs-lookup"><span data-stu-id="c981f-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="c981f-105">Die übergeordnete Klasse, von der alle System Ereignis-Ablauf Verfolgungs Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c981f-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="c981f-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c981f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c981f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c981f-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="c981f-108">Member</span><span class="sxs-lookup"><span data-stu-id="c981f-108">Members</span></span>

<span data-ttu-id="c981f-109">Die **MSNT \_ systemtrace** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c981f-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="c981f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c981f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c981f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c981f-111">Properties</span></span>

<span data-ttu-id="c981f-112">Die **MSNT \_ systemtrace** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c981f-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c981f-113">**Flags**</span><span class="sxs-lookup"><span data-stu-id="c981f-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c981f-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c981f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c981f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c981f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c981f-116">Qualifizierer: **definevalues {"ereignisablaufverfolgungsflag \_ \_ \_ verarbeiten", "ereignisablaufverfolgungsflag-Thread", "ereignisablaufverfolgungsflag zum Laden von Ereignissen", "Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Prozess \_ Zähler" Ereignis Ablaufverfolgungsflag für Datenträger-e/a \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ "," Ereignis Ablauf \_ Verfolgung Flag Datenträger Datei-e/a " \_ \_ \_ \_ ," Ereignis Ablaufverfolgungsflag für Datenträger-e/a-Vorgänge \_ \_ \_ \_ \_ "," \_ \_ \_ ereignisablaufverfolgungsflag-Verteiler "," Ereignis Ablauf Verfolgung \_ Flag Arbeits \_ \_ Speicher \_ Seiten \_ Fehler "ereignisablaufverfolgungsflag- \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Registrierung", "ereignisablaufverfolgungsflag \_ \_ \_ ALPC", "Ereignis Ablaufverfolgungsflag \_ \_ \_ Split IO", "ereignisablaufverfolgungsflag-Treiber", "ereignisablaufverfolgungsflag- \_ \_ \_ \_ \_ \_ \_ Profil", "ereignisablaufverfolgungsflag für \_ \_ \_ Datei \_ \_ \_ \_ \_ \_** **map {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000 bis", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span><span class="sxs-lookup"><span data-stu-id="c981f-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="c981f-117">Aktivieren Sie das Flag, das die aktivierten Kernel Anbieter angibt.</span><span class="sxs-lookup"><span data-stu-id="c981f-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c981f-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c981f-118">Requirements</span></span>



| <span data-ttu-id="c981f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c981f-119">Requirement</span></span> | <span data-ttu-id="c981f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c981f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c981f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c981f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c981f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c981f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c981f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c981f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c981f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c981f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




