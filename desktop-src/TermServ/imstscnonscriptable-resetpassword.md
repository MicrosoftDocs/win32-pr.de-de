---
title: Imstscnonscriptable ResetPassword-Methode
description: Setzt alle Kenn Wort Zustände im Remotedesktop ActiveX-Steuerelement zurück.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- ResetPassword-Methode Remotedesktopdienste
- ResetPassword-Methode Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, ResetPassword-Methode
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478882"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="39d5f-106">Imstscnonscriptable:: ResetPassword-Methode</span><span class="sxs-lookup"><span data-stu-id="39d5f-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="39d5f-107">Setzt alle Kenn Wort Zustände im Remotedesktop ActiveX-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="39d5f-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="39d5f-108">Sie können diese Methode aufrufen, um Kenn Wörter zu löschen, die in einem der drei unterstützten Formate gespeichert sind: Klartext, portabel codiert oder Binär (nicht portabel) codiert.</span><span class="sxs-lookup"><span data-stu-id="39d5f-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="39d5f-109">Beachten Sie, dass codierte Kenn Wörter nicht als sicher verschlüsselt angesehen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="39d5f-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d5f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d5f-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="39d5f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39d5f-111">Parameters</span></span>

<span data-ttu-id="39d5f-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="39d5f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39d5f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39d5f-113">Return value</span></span>

<span data-ttu-id="39d5f-114">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="39d5f-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d5f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39d5f-115">Remarks</span></span>

<span data-ttu-id="39d5f-116">Sie können diese Methode zum Zurücksetzen des Kennworts für das Steuerelement nach dem Trennen der Verbindung abrufen.</span><span class="sxs-lookup"><span data-stu-id="39d5f-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="39d5f-117">Dadurch wird sichergestellt, dass nachfolgende Verbindungen, die dieselbe Instanz des Steuer Elements verwenden, sich nicht automatisch mit einem zuvor festgelegten Kennwort anmelden.</span><span class="sxs-lookup"><span data-stu-id="39d5f-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="39d5f-118">Diese Methode kann nur aufgerufen werden, wenn sich das Remotedesktop ActiveX-Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="39d5f-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="39d5f-119">Diese Methode gibt **E \_ Fail** zurück, wenn Sie aufgerufen wird, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="39d5f-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="39d5f-120">Um den verbundenen Status zu überprüfen, müssen Sie die [**get \_ Connected**](imstscax-connected.md) -Methode über die [**imstscax**](imstscax-interface.md) -Schnittstelle oder eine der Schnittstellen, die von ihr erbt, abrufen.</span><span class="sxs-lookup"><span data-stu-id="39d5f-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="39d5f-121">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="39d5f-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39d5f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39d5f-122">Requirements</span></span>



| <span data-ttu-id="39d5f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39d5f-123">Requirement</span></span> | <span data-ttu-id="39d5f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="39d5f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39d5f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39d5f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39d5f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39d5f-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="39d5f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39d5f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39d5f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39d5f-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="39d5f-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="39d5f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="39d5f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d5f-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="39d5f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="39d5f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d5f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d5f-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="39d5f-133">IID</span><span class="sxs-lookup"><span data-stu-id="39d5f-133">IID</span></span><br/>                      | <span data-ttu-id="39d5f-134">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="39d5f-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39d5f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39d5f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d5f-136">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="39d5f-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





