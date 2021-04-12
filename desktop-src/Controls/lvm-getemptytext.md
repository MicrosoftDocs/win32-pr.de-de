---
title: LVM_GETEMPTYTEXT Meldung (kommstrg. h)
description: Ruft den Text ab, der für die Anzeige bestimmt ist, wenn das Listenansicht-Steuerelement leer erscheint. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getemptytext-Makros.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Windows-Steuerelemente für LVM_GETEMPTYTEXT Meldung
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475168"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="de526-105">LVM- \_ getemptytext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="de526-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="de526-106">Ruft den Text ab, der für die Anzeige bestimmt ist, wenn das Listenansicht-Steuerelement leer erscheint.</span><span class="sxs-lookup"><span data-stu-id="de526-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="de526-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getemptytext**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) -Makros.</span><span class="sxs-lookup"><span data-stu-id="de526-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="de526-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de526-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de526-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de526-110">Die Größe des Puffers, auf den *LPARAM* zeigt, einschließlich des abschließenden **null**-Werte.</span><span class="sxs-lookup"><span data-stu-id="de526-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="de526-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de526-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de526-112">Ein Zeiger auf einen null-terminierten Unicode-Puffer der Größe, der von *wParam* angegeben wird, um den Text zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="de526-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="de526-113">Der Aufrufer ist für die Zuordnung des Puffers verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="de526-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de526-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de526-114">Return value</span></span>

<span data-ttu-id="de526-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="de526-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de526-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de526-116">Requirements</span></span>



| <span data-ttu-id="de526-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de526-117">Requirement</span></span> | <span data-ttu-id="de526-118">Wert</span><span class="sxs-lookup"><span data-stu-id="de526-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de526-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de526-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de526-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de526-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de526-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de526-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de526-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de526-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de526-123">Header</span><span class="sxs-lookup"><span data-stu-id="de526-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de526-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de526-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





