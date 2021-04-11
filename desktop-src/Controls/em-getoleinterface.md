---
title: EM_GETOLEINTERFACE Meldung (RichEdit. h)
description: Ruft ein iricheditole-Objekt ab, mit dem ein Client auf die Component Object Model (com)-Funktionalität eines Rich-Edit-Steuer Elements zugreifen kann.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Windows-Steuerelemente für EM_GETOLEINTERFACE Meldung
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104817"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="cb813-104">EM \_ getoleinterface-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cb813-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="cb813-105">Ruft ein [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Objekt ab, mit dem ein Client auf die Component Object Model (com)-Funktionalität eines Rich-Edit-Steuer Elements zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="cb813-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb813-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb813-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb813-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb813-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="cb813-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb813-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb813-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb813-110">Zeiger auf einen Zeiger, der das [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="cb813-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="cb813-111">Das-Steuerelement ruft vor der Rückgabe die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode für das-Objekt auf, sodass die aufrufende Anwendung die [**releasemethode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufrufen muss, wenn Sie mit dem-Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb813-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb813-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb813-112">Return value</span></span>

<span data-ttu-id="cb813-113">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cb813-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cb813-114">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cb813-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb813-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb813-115">Requirements</span></span>



| <span data-ttu-id="cb813-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb813-116">Requirement</span></span> | <span data-ttu-id="cb813-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cb813-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb813-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb813-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb813-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb813-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb813-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb813-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb813-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb813-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb813-122">Header</span><span class="sxs-lookup"><span data-stu-id="cb813-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb813-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb813-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb813-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb813-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb813-125">**Iricheditole**</span><span class="sxs-lookup"><span data-stu-id="cb813-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

