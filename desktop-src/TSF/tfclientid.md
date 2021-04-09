---
title: Tfclientid (msctf. h)
description: Der tfclientid-Datentyp wird verwendet, um den Client zu identifizieren.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- Tfclientid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740873"
---
# <a name="tfclientid"></a><span data-ttu-id="36f73-104">Tfclientid</span><span class="sxs-lookup"><span data-stu-id="36f73-104">TfClientId</span></span>

<span data-ttu-id="36f73-105">Der **tfclientid-** Datentyp wird verwendet, um den Client zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="36f73-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="36f73-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36f73-106">Remarks</span></span>

<span data-ttu-id="36f73-107">In TSF werden Anwendungen und Text Dienste im Allgemeinen als Clients bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="36f73-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="36f73-108">Jeder Client erhält einen eindeutigen Bezeichner, den er verwendet, um sich selbst zu identifizieren, wenn verschiedene TSF Manager-Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="36f73-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="36f73-109">Dieser Bezeichner weist den **tfclientid-** Typ auf.</span><span class="sxs-lookup"><span data-stu-id="36f73-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="36f73-110">Der **tfclientid-** Datentyp wird vom TSF-Manager bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="36f73-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="36f73-111">Eine Anwendung erhält einen **tfclientid-** Wert, wenn [ITfThreadMgr:: Aktivierung](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="36f73-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="36f73-112">Der tfclientid-Wert für einen Text Dienst wird an die [itftextinputprocessor:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="36f73-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="36f73-113">Alle Objekte, die nicht in die obigen Kategorien passen, können durch Aufrufen von [itfclientid:: getClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)einen Client Bezeichner abrufen.</span><span class="sxs-lookup"><span data-stu-id="36f73-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="36f73-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36f73-114">Requirements</span></span>



| <span data-ttu-id="36f73-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36f73-115">Requirement</span></span> | <span data-ttu-id="36f73-116">Wert</span><span class="sxs-lookup"><span data-stu-id="36f73-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="36f73-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36f73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36f73-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="36f73-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="36f73-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36f73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36f73-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="36f73-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="36f73-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="36f73-121">Redistributable</span></span><br/>          | <span data-ttu-id="36f73-122">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36f73-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="36f73-123">Header</span><span class="sxs-lookup"><span data-stu-id="36f73-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36f73-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f73-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="36f73-125">IDL</span><span class="sxs-lookup"><span data-stu-id="36f73-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36f73-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36f73-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f73-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36f73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f73-128">**ITF ClientID:: getClientID**</span><span class="sxs-lookup"><span data-stu-id="36f73-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="36f73-129">**ITF textinputprocessor:: Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="36f73-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="36f73-130">**ITfThreadMgr:: Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="36f73-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





