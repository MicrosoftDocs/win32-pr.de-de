---
title: Benachrichtigungs Code für NM_NCHITTEST (Rebar) (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine WM- \_ nchittest-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Windows-Steuerelemente für die NM_NCHITTEST (Info Leiste)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105098"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="39242-105">NM \_ nchittest (Info Leiste)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="39242-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="39242-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="39242-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="39242-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="39242-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39242-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39242-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39242-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39242-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39242-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="39242-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="39242-111">Der **dwitemspec** -Member enthält den BandIndex, über den die Treffer Testnachricht aufgetreten ist, und das **PT** -Element enthält die Maus Koordinaten der Treffer Testnachricht.</span><span class="sxs-lookup"><span data-stu-id="39242-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39242-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39242-112">Return value</span></span>

<span data-ttu-id="39242-113">Gibt NULL zurück, damit die Überprüfung die Standard Verarbeitung der Treffer Testnachricht durchführen kann, oder gibt einen der HT-Werte zurück, der \* unter [**WM \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) dokumentiert ist, um die standardmäßige Treffer Testverarbeitung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="39242-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="39242-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39242-114">Requirements</span></span>



| <span data-ttu-id="39242-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39242-115">Requirement</span></span> | <span data-ttu-id="39242-116">Wert</span><span class="sxs-lookup"><span data-stu-id="39242-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39242-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39242-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39242-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39242-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39242-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39242-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39242-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39242-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39242-121">Header</span><span class="sxs-lookup"><span data-stu-id="39242-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="39242-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="39242-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

