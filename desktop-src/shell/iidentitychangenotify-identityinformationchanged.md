---
description: Identityinformationchanged wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Iidentitychangenotify:: identityinformationchanged-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864903"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="16ed2-104">Iidentitychangenotify:: identityinformationchanged-Methode</span><span class="sxs-lookup"><span data-stu-id="16ed2-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="16ed2-105">\[**Identityinformationchanged** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="16ed2-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="16ed2-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="16ed2-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="16ed2-107">Wird aufgerufen, wenn sich die Informationen zu einer Benutzeridentität geändert haben oder wenn eine Benutzeridentität hinzugefügt oder gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="16ed2-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ed2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16ed2-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="16ed2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16ed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ed2-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="16ed2-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="16ed2-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="16ed2-111">Type: **DWORD**</span></span>

<span data-ttu-id="16ed2-112">Ein-Wert, der den Typ der geänderten Informationen oder den für eine Identität ausgeführten Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="16ed2-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="16ed2-113">Kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="16ed2-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="16ed2-114">(IIC \_ aktuelle \_ Identität \_ geändert)</span><span class="sxs-lookup"><span data-stu-id="16ed2-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="16ed2-115">Die aktuelle Identität wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="16ed2-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="16ed2-116">(IIC \_ Identität \_ geändert)</span><span class="sxs-lookup"><span data-stu-id="16ed2-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="16ed2-117">Eine Identität wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="16ed2-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="16ed2-118">(IIC \_ Identität \_ gelöscht)</span><span class="sxs-lookup"><span data-stu-id="16ed2-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="16ed2-119">Eine Identität wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="16ed2-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="16ed2-120">(IIC \_ Identität \_ hinzugefügt)</span><span class="sxs-lookup"><span data-stu-id="16ed2-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="16ed2-121">Es wurde eine neue Identität hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="16ed2-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ed2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16ed2-122">Return value</span></span>

<span data-ttu-id="16ed2-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16ed2-123">Type: **HRESULT**</span></span>

<span data-ttu-id="16ed2-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="16ed2-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16ed2-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16ed2-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16ed2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16ed2-126">Remarks</span></span>

<span data-ttu-id="16ed2-127">Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn die Liste der Benutzer Identitäten im System geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="16ed2-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ed2-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="16ed2-128">Requirements</span></span>



| <span data-ttu-id="16ed2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16ed2-129">Requirement</span></span> | <span data-ttu-id="16ed2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="16ed2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16ed2-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16ed2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="16ed2-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16ed2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16ed2-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16ed2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="16ed2-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16ed2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16ed2-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="16ed2-135">End of client support</span></span><br/>    | <span data-ttu-id="16ed2-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="16ed2-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="16ed2-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="16ed2-137">End of server support</span></span><br/>    | <span data-ttu-id="16ed2-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16ed2-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="16ed2-139">Header</span><span class="sxs-lookup"><span data-stu-id="16ed2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="16ed2-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="16ed2-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="16ed2-141">IDL</span><span class="sxs-lookup"><span data-stu-id="16ed2-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16ed2-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16ed2-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="16ed2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="16ed2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16ed2-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16ed2-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




