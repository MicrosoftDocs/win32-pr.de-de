---
title: Tfeditcookie (msctf. h)
description: Der tfeditcookie-Datentyp identifiziert eine Bearbeitungs Sitzung, die über eine Sperre verfügt.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- Tfeditcookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040060"
---
# <a name="tfeditcookie"></a><span data-ttu-id="cd815-104">Tfeditcookie</span><span class="sxs-lookup"><span data-stu-id="cd815-104">TfEditCookie</span></span>

<span data-ttu-id="cd815-105">Der **tfeditcookie** -Datentyp identifiziert eine Bearbeitungs Sitzung, die über eine Sperre verfügt.</span><span class="sxs-lookup"><span data-stu-id="cd815-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="cd815-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd815-106">Remarks</span></span>

<span data-ttu-id="cd815-107">Der **tfeditcookie** -Datentyp wird vom TSF-Manager bereitgestellt und wird von einem Client (Anwendungs-oder Text Dienst) verwendet, um eine Bearbeitungs Sitzung mit einer Lese-oder Lese-/Schreibsperre in verschiedenen Methoden zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd815-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="cd815-108">Ein **tfeditcookie** -Wert wird auf eine der folgenden Arten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cd815-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="cd815-109">Der Client ruft [ITF documentmgr:: featecontext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)auf.</span><span class="sxs-lookup"><span data-stu-id="cd815-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="cd815-110">Der TSF-Manager ruft die Client- [itfedizession::D oedizession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="cd815-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="cd815-111">Der TSF-Manager ruft die [ITF compositionsink:: oncompositionbeendete](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) -Methode des Clients auf.</span><span class="sxs-lookup"><span data-stu-id="cd815-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="cd815-112">Der TSF-Manager ruft die [ITF cleanupcontextsink:: oncleanupcontext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) -Methode des Clients auf.</span><span class="sxs-lookup"><span data-stu-id="cd815-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="cd815-113">Der TSF-Manager ruft die [itbtexteditsink:: onendedit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) -Client Methode auf.</span><span class="sxs-lookup"><span data-stu-id="cd815-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd815-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd815-114">Requirements</span></span>



| <span data-ttu-id="cd815-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd815-115">Requirement</span></span> | <span data-ttu-id="cd815-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cd815-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd815-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd815-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd815-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cd815-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="cd815-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd815-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd815-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cd815-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="cd815-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cd815-121">Redistributable</span></span><br/>          | <span data-ttu-id="cd815-122">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd815-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="cd815-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd815-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd815-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd815-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd815-125">IDL</span><span class="sxs-lookup"><span data-stu-id="cd815-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd815-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd815-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd815-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd815-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd815-128">**ITF cleanupcontextsink:: oncleanupcontext**</span><span class="sxs-lookup"><span data-stu-id="cd815-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="cd815-129">**ITF compositionsink:: oncompositionbeendete**</span><span class="sxs-lookup"><span data-stu-id="cd815-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="cd815-130">**ITF documentmgr:: kreatecontext**</span><span class="sxs-lookup"><span data-stu-id="cd815-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="cd815-131">**Itfedizession::D oedizession**</span><span class="sxs-lookup"><span data-stu-id="cd815-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="cd815-132">**ITF texteditsink:: onendedit**</span><span class="sxs-lookup"><span data-stu-id="cd815-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





