---
title: EM_SETOLECALLBACK Meldung (RichEdit. h)
description: Ermöglicht einem Rich-Edit-Steuerelement ein IRichEditOleCallback-Objekt, das das Steuerelement verwendet, um OLE-bezogene Ressourcen und Informationen vom Client abzurufen.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Windows-Steuerelemente für EM_SETOLECALLBACK Meldung
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956637"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="4173b-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="4173b-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="4173b-105">Ermöglicht einem Rich-Edit-Steuerelement ein [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Objekt, das das Steuerelement verwendet, um OLE-bezogene Ressourcen und Informationen vom Client abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4173b-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="4173b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4173b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4173b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4173b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4173b-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4173b-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4173b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4173b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4173b-110">Zeiger auf ein [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4173b-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="4173b-111">Das-Steuerelement ruft vor der Rückgabe die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode für das-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="4173b-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4173b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4173b-112">Return value</span></span>

<span data-ttu-id="4173b-113">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4173b-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4173b-114">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4173b-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4173b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4173b-115">Requirements</span></span>



| <span data-ttu-id="4173b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4173b-116">Requirement</span></span> | <span data-ttu-id="4173b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4173b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4173b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4173b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4173b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4173b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4173b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4173b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4173b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4173b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4173b-122">Header</span><span class="sxs-lookup"><span data-stu-id="4173b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4173b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4173b-123"><dt>Richedit.h</dt></span></span> </dl> |



 

