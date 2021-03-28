---
description: Hebt die Registrierung einer appbar auf, indem Sie aus der internen Liste des Systems entfernt wird. Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden.
title: ABM_REMOVE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862139"
---
# <a name="abm_remove-message"></a><span data-ttu-id="604b2-104">ABM \_ Entfernungs Meldung</span><span class="sxs-lookup"><span data-stu-id="604b2-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="604b2-105">Hebt die Registrierung einer appbar auf, indem Sie aus der internen Liste des Systems entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="604b2-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="604b2-106">Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="604b2-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="604b2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="604b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604b2-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="604b2-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="604b2-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die das Handle für die APP-Leiste enthält, deren Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="604b2-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="604b2-110">Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="604b2-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604b2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="604b2-111">Return value</span></span>

<span data-ttu-id="604b2-112">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="604b2-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="604b2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="604b2-113">Remarks</span></span>

<span data-ttu-id="604b2-114">Diese Meldung bewirkt, dass das System die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung an alle appbars sendet.</span><span class="sxs-lookup"><span data-stu-id="604b2-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="604b2-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="604b2-115">Requirements</span></span>



| <span data-ttu-id="604b2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="604b2-116">Requirement</span></span> | <span data-ttu-id="604b2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="604b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="604b2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="604b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="604b2-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="604b2-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="604b2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="604b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="604b2-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="604b2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="604b2-122">Header</span><span class="sxs-lookup"><span data-stu-id="604b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="604b2-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="604b2-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




