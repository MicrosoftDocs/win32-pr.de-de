---
description: Die handofftable-Struktur definiert die Protokolle einer Übergabe-Tabelle.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Handofftable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344658"
---
# <a name="handofftable-structure"></a><span data-ttu-id="c59de-103">Handofftable-Struktur</span><span class="sxs-lookup"><span data-stu-id="c59de-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="c59de-104">Die **handofftable** -Struktur definiert die Protokolle einer Übergabe-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c59de-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="c59de-105">Diese Struktur wird von Netzwerkmonitor basierend auf Informationen in einer vom Benutzer bereitgestellten ini-Datei ausgefüllt, die beim Aufrufen der [**createhandofftable**](createhandofftable.md) -Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c59de-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c59de-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="c59de-107">Member</span><span class="sxs-lookup"><span data-stu-id="c59de-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c59de-108">**heiße \_ sig**</span><span class="sxs-lookup"><span data-stu-id="c59de-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="c59de-109">Die Signatur, die diese Tabelle als eine Übergabe Tabelle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c59de-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="c59de-110">**heiße \_ numentries**</span><span class="sxs-lookup"><span data-stu-id="c59de-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c59de-111">Anzahl von Einträgen, die der Übergabe Tabelle Netzwerkmonitor hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c59de-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="c59de-112">**Hot- \_ Einträge**</span><span class="sxs-lookup"><span data-stu-id="c59de-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="c59de-113">Handoff-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c59de-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c59de-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59de-114">Remarks</span></span>

<span data-ttu-id="c59de-115">Diese Struktur und die zugehörigen handoffentry-Strukturen werden durch Netzwerkmonitor ausgefüllt, wenn Netzwerkmonitor eine Übergabe Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="c59de-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="c59de-116">Die Protokollinformationen, die beim Erstellen einer Übergabe Tabelle verwendet werden, werden in einer INI-Datei bereitgestellt, die von der Anwendung bereitgestellt wird, wenn " [**deehandofftable**](createhandofftable.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c59de-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59de-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c59de-117">Requirements</span></span>



| <span data-ttu-id="c59de-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c59de-118">Requirement</span></span> | <span data-ttu-id="c59de-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c59de-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c59de-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c59de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c59de-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c59de-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c59de-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c59de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c59de-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c59de-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c59de-124">Header</span><span class="sxs-lookup"><span data-stu-id="c59de-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c59de-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59de-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59de-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c59de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59de-127">Handoffentry</span><span class="sxs-lookup"><span data-stu-id="c59de-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="c59de-128">"Kreatehandofftable"</span><span class="sxs-lookup"><span data-stu-id="c59de-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




