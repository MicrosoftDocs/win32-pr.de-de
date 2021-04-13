---
title: SendMessage-Methode der Win32_VirtualDesktopSession-Klasse
description: Senden Sie eine Nachricht über die virtuelle Desktop Sitzung an den Benutzer.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage-Methode Remotedesktopdienste
- SendMessage-Methode Remotedesktopdienste, Win32_VirtualDesktopSession-Klasse
- Win32_VirtualDesktopSession-Klasse Remotedesktopdienste, SendMessage-Methode
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391869"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="dde62-106">SendMessage-Methode der Win32 \_ virtualdesktopsession-Klasse</span><span class="sxs-lookup"><span data-stu-id="dde62-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="dde62-107">Senden Sie eine Nachricht über die virtuelle Desktop Sitzung an den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="dde62-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dde62-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="dde62-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dde62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde62-110">*Titel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dde62-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde62-111">Der Titel der Messung.</span><span class="sxs-lookup"><span data-stu-id="dde62-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="dde62-112">*Nachricht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dde62-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde62-113">Der Inhalt der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dde62-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde62-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dde62-114">Return value</span></span>

<span data-ttu-id="dde62-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dde62-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde62-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dde62-116">Requirements</span></span>



| <span data-ttu-id="dde62-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dde62-117">Requirement</span></span> | <span data-ttu-id="dde62-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dde62-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde62-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dde62-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dde62-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dde62-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dde62-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dde62-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dde62-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dde62-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="dde62-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="dde62-123">Namespace</span></span><br/>                | <span data-ttu-id="dde62-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="dde62-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dde62-125">MOF</span><span class="sxs-lookup"><span data-stu-id="dde62-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dde62-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dde62-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dde62-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dde62-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dde62-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dde62-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dde62-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde62-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde62-130">**Win32 \_ virtualdesktopsession**</span><span class="sxs-lookup"><span data-stu-id="dde62-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





