---
title: TB_BUTTONSTRUCTSIZE Meldung (kommstrg. h)
description: Gibt die Größe der TBBUTTON-Struktur an.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Windows-Steuerelemente für TB_BUTTONSTRUCTSIZE Meldung
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041015"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="5cc4b-104">TB \_ buttonstructsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="5cc4b-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="5cc4b-105">Gibt die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cc4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cc4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc4b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cc4b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cc4b-108">Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5cc4b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cc4b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5cc4b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc4b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cc4b-111">Return value</span></span>

<span data-ttu-id="5cc4b-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc4b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cc4b-113">Remarks</span></span>

<span data-ttu-id="5cc4b-114">Das System verwendet die Größe, um zu bestimmen, welche Version der Common Control Dynamic Link Library (dll) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="5cc4b-115">Wenn eine Anwendung die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwendet, um die Symbolleiste zu erstellen, muss die Anwendung diese Nachricht vor dem Senden der Meldung " [**TB \_ AddBitmap**](tb-addbitmap.md) " oder " [**TB \_ AddButtons**](tb-addbuttons.md) " an die Symbolleiste senden.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="5cc4b-116">Die Funktion " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " sendet automatisch **TB " \_ buttonstructsize**", und die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur ist ein Parameter der Funktion.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc4b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cc4b-117">Requirements</span></span>



| <span data-ttu-id="5cc4b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cc4b-118">Requirement</span></span> | <span data-ttu-id="5cc4b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5cc4b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc4b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5cc4b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc4b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cc4b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cc4b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5cc4b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc4b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cc4b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc4b-124">Header</span><span class="sxs-lookup"><span data-stu-id="5cc4b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc4b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc4b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

