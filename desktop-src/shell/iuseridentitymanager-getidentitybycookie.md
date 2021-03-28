---
description: Getidentitybycookie wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Iuseridentitymanager:: getidentitybycookie-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524440"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="9c989-104">Iuseridentitymanager:: getidentitybycookie-Methode</span><span class="sxs-lookup"><span data-stu-id="9c989-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="9c989-105">\[**Getidentitybycookie** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9c989-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9c989-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="9c989-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="9c989-107">Ruft eine bestimmte Benutzeridentität durch das Cookie ab, das zur eindeutigen Identifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c989-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c989-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c989-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="9c989-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c989-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c989-110">*uidcookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c989-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c989-111">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="9c989-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="9c989-112">Die Adresse eines _ \*GUID\*\*-Werts, der das Cookie für die Identität darstellt, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c989-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9c989-113">*ppIdentity* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9c989-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c989-114">Type: **[ **iuseridentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9c989-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="9c989-115">Die Adresse des Zeigers, der das Benutzer Identitäts Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="9c989-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c989-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c989-116">Return value</span></span>

<span data-ttu-id="9c989-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c989-117">Type: **HRESULT**</span></span>

<span data-ttu-id="9c989-118">Das Ergebnis der Abruf Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9c989-118">The result of the retrieval request.</span></span> <span data-ttu-id="9c989-119">Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="9c989-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="9c989-120">Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c989-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="9c989-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9c989-121">Return code</span></span>                                                                                            | <span data-ttu-id="9c989-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c989-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="9c989-123"><dt>**E- \_ Identität \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="9c989-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="9c989-124">Die angeforderte Identität konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="9c989-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="9c989-125"><dt>**E- \_ Identitäten \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="9c989-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="9c989-126">Die Identitätsverwaltung ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9c989-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9c989-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9c989-127">Requirements</span></span>



| <span data-ttu-id="9c989-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c989-128">Requirement</span></span> | <span data-ttu-id="9c989-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9c989-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c989-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c989-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c989-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c989-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c989-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c989-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c989-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c989-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c989-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9c989-134">End of client support</span></span><br/>    | <span data-ttu-id="9c989-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9c989-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9c989-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9c989-136">End of server support</span></span><br/>    | <span data-ttu-id="9c989-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c989-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9c989-138">Header</span><span class="sxs-lookup"><span data-stu-id="9c989-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c989-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c989-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c989-140">IDL</span><span class="sxs-lookup"><span data-stu-id="9c989-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c989-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c989-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="9c989-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9c989-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c989-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c989-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




