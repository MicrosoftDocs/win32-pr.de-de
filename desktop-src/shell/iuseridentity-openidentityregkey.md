---
description: Veraltet. Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Iuseridentity:: openidentityregkey-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977896"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="61439-104">Iuseridentity:: openidentityregkey-Methode</span><span class="sxs-lookup"><span data-stu-id="61439-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="61439-105">\[Die **iuseridentity:: openidentityregkey** -Methode ist für die Verwendung in Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61439-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="61439-106">In Windows XP wurde diese Funktion durch [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md)abgelöst und kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="61439-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="61439-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="61439-107">Deprecated.</span></span> <span data-ttu-id="61439-108">Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.</span><span class="sxs-lookup"><span data-stu-id="61439-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="61439-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="61439-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="61439-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61439-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61439-111">*dwDesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61439-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61439-112">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="61439-112">Type: **DWORD**</span></span>

<span data-ttu-id="61439-113">Ein-Wert, der die angeforderte Zugriffsebene für den Registrierungsschlüssel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="61439-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="61439-114">*phkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61439-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61439-115">Geben Sie Folgendes ein: \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="61439-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="61439-116">Ein Zeiger, der den Registrierungsschlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="61439-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61439-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61439-117">Return value</span></span>

<span data-ttu-id="61439-118">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="61439-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="61439-119">Das Ergebnis der Registrierungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61439-119">The result of the registry request.</span></span> <span data-ttu-id="61439-120">Bei erfolgreicher Ausführung wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61439-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="61439-121">Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61439-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="61439-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="61439-122">Return code</span></span>                                                                                            | <span data-ttu-id="61439-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61439-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="61439-124"><dt>**E- \_ Identität \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="61439-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="61439-125">Diese Identität weist keinen zugeordneten Registrierungsschlüssel auf.</span><span class="sxs-lookup"><span data-stu-id="61439-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="61439-126"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="61439-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="61439-127">Der Zugriff auf den Registrierungsschlüssel war nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="61439-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="61439-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61439-128">Remarks</span></span>

<span data-ttu-id="61439-129">Der *dwDesiredAccess* -Parameter ist eine standardmäßige Registrierungs Zugriffs-Sicherheits Beschreibung, die den Zugriff beschreibt, den Sie für den Registrierungsschlüssel gewinnen möchten.</span><span class="sxs-lookup"><span data-stu-id="61439-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="61439-130">Weitere Informationen zur Registrierungs Sicherheit, einschließlich einer Liste zulässiger Werte für diesen Parameter, finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="61439-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61439-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="61439-131">Requirements</span></span>



| <span data-ttu-id="61439-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61439-132">Requirement</span></span> | <span data-ttu-id="61439-133">Wert</span><span class="sxs-lookup"><span data-stu-id="61439-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61439-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61439-134">Minimum supported client</span></span><br/> | <span data-ttu-id="61439-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61439-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61439-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61439-136">Minimum supported server</span></span><br/> | <span data-ttu-id="61439-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61439-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="61439-138">Header</span><span class="sxs-lookup"><span data-stu-id="61439-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="61439-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="61439-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="61439-140">IDL</span><span class="sxs-lookup"><span data-stu-id="61439-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61439-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61439-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="61439-142">DLL</span><span class="sxs-lookup"><span data-stu-id="61439-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61439-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61439-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61439-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61439-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61439-145">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="61439-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="61439-146">**Iuseridentity:: getidentityfolder**</span><span class="sxs-lookup"><span data-stu-id="61439-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
