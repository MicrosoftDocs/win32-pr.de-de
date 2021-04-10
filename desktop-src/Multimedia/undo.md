---
title: Befehl rückgängig
description: Der Befehl rückgängig kehrt die Aktion um, die durch den letzten erfolgreichen Kopier-, Ausschneide-, Lösch-, rückgängig-oder Einfügebefehl ausgeführt wird Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- Befehl "Rückgängig" Windows Multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040973"
---
# <a name="undo-command"></a><span data-ttu-id="bd77f-105">Befehl rückgängig</span><span class="sxs-lookup"><span data-stu-id="bd77f-105">undo command</span></span>

<span data-ttu-id="bd77f-106">Der Befehl rückgängig kehrt die Aktion um, die durch den letzten erfolgreichen [Kopier](copy.md)-, Ausschneide-, [Lösch](delete.md)-, rückgängig [-oder](paste.md) [Einfügebefehl](cut.md)ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="bd77f-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="bd77f-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="bd77f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="bd77f-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="bd77f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="bd77f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd77f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd77f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="bd77f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bd77f-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="bd77f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="bd77f-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bd77f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="bd77f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="bd77f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bd77f-114">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="bd77f-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="bd77f-115">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bd77f-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd77f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd77f-116">Return Value</span></span>

<span data-ttu-id="bd77f-117">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="bd77f-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd77f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd77f-118">Requirements</span></span>



| <span data-ttu-id="bd77f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd77f-119">Requirement</span></span> | <span data-ttu-id="bd77f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bd77f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bd77f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd77f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd77f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd77f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bd77f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd77f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd77f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd77f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bd77f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd77f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd77f-126">MCI</span><span class="sxs-lookup"><span data-stu-id="bd77f-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bd77f-127">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="bd77f-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="bd77f-128">copy</span><span class="sxs-lookup"><span data-stu-id="bd77f-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="bd77f-129">Schnitts</span><span class="sxs-lookup"><span data-stu-id="bd77f-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="bd77f-130">delete</span><span class="sxs-lookup"><span data-stu-id="bd77f-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="bd77f-131">kle</span><span class="sxs-lookup"><span data-stu-id="bd77f-131">paste</span></span>](paste.md)
</dt> </dl>

 

