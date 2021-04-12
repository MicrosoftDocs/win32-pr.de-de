---
title: LVM_GETGROUPINFOBYINDEX Meldung (kommstrg. h)
description: Ruft Informationen zu einer angegebenen Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgroupinfobyindex-Makros.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Windows-Steuerelemente für LVM_GETGROUPINFOBYINDEX Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104457"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="5939b-105">LVM \_ getgroupinfobyindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="5939b-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="5939b-106">Ruft Informationen zu einer angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5939b-106">Gets information on a specified group.</span></span> <span data-ttu-id="5939b-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgroupinfobyindex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) -Makros.</span><span class="sxs-lookup"><span data-stu-id="5939b-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5939b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5939b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5939b-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5939b-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5939b-110">Der Index der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5939b-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5939b-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5939b-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5939b-112">Ein Zeiger auf eine [**orgroup**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) -Struktur, die Informationen über die von *wParam* angegebene Gruppe empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="5939b-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="5939b-113">Der aufrufende Prozess ist für die Zuordnung von Arbeitsspeicher für die Struktur und alle Puffer in der Struktur verantwortlich, wie z. b. den, auf den das **pszheader** -Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="5939b-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="5939b-114">Legen Sie alle Kontingenten Elemente der Struktur fest, z. b. **cchheader** die Größe des Puffers, auf den **pszheader** in **WCHARs** zeigt, einschließlich des abschließenden **null**-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5939b-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="5939b-115">Legen Sie **CBSIZE** auf sizeof (LVGROUP) fest.</span><span class="sxs-lookup"><span data-stu-id="5939b-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="5939b-116">Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmember mit Informationen für die von *wParam* angegebene Gruppe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5939b-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5939b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5939b-117">Return value</span></span>

<span data-ttu-id="5939b-118">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5939b-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5939b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5939b-119">Requirements</span></span>



| <span data-ttu-id="5939b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5939b-120">Requirement</span></span> | <span data-ttu-id="5939b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5939b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5939b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5939b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5939b-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5939b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5939b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5939b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5939b-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5939b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5939b-126">Header</span><span class="sxs-lookup"><span data-stu-id="5939b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5939b-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5939b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





