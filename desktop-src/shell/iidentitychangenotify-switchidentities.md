---
description: Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Iidentitychangenotify:: switchidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994598"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="cce09-103">Iidentitychangenotify:: switchidentities-Methode</span><span class="sxs-lookup"><span data-stu-id="cce09-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="cce09-104">\[**Switchidentities** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cce09-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cce09-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cce09-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="cce09-106">Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="cce09-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce09-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cce09-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="cce09-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cce09-108">Parameters</span></span>

<span data-ttu-id="cce09-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cce09-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cce09-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cce09-110">Return value</span></span>

<span data-ttu-id="cce09-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cce09-111">Type: **HRESULT**</span></span>

<span data-ttu-id="cce09-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cce09-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cce09-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cce09-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce09-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cce09-114">Remarks</span></span>

<span data-ttu-id="cce09-115">Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn ein Benutzer die Identitäten erfolgreich gewechselt hat.</span><span class="sxs-lookup"><span data-stu-id="cce09-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="cce09-116">Um benutzerdefiniertes Verhalten bereitzustellen, bevor ein Benutzer Identitätswechsel stattfindet, implementieren Sie die [**iidentitychangenotify:: queryswitchidentities**](iidentitychangenotify-queryswitchidentities.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cce09-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce09-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cce09-117">Requirements</span></span>



| <span data-ttu-id="cce09-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cce09-118">Requirement</span></span> | <span data-ttu-id="cce09-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cce09-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cce09-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cce09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cce09-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cce09-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cce09-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cce09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cce09-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cce09-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cce09-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cce09-124">End of client support</span></span><br/>    | <span data-ttu-id="cce09-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cce09-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="cce09-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cce09-126">End of server support</span></span><br/>    | <span data-ttu-id="cce09-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cce09-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="cce09-128">Header</span><span class="sxs-lookup"><span data-stu-id="cce09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce09-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce09-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="cce09-130">IDL</span><span class="sxs-lookup"><span data-stu-id="cce09-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cce09-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cce09-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="cce09-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cce09-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cce09-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cce09-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cce09-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cce09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce09-135">**Iidentitychangenotify**</span><span class="sxs-lookup"><span data-stu-id="cce09-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="cce09-136">**Iidentitychangenotify:: queryswitchidentities**</span><span class="sxs-lookup"><span data-stu-id="cce09-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




