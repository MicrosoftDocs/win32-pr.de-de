---
title: Dssetauthidentity-Funktion (ntdsbcli. h)
description: Legt den Sicherheitskontext fest, unter dem die APIs für die Verzeichnis Sicherung aufgerufen werden.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Dssetauthidentity-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477343"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="77874-104">Dssetauthidentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="77874-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="77874-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="77874-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="77874-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="77874-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="77874-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="77874-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="77874-108">Die **dssetauthidentity** -Funktion legt den Sicherheitskontext fest, unter dem die Verzeichnis Sicherungs-APIs aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="77874-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="77874-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77874-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="77874-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="77874-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77874-111">*szusername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77874-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77874-112">Die NULL-terminierte Zeichenfolge, die den Benutzernamen angibt.</span><span class="sxs-lookup"><span data-stu-id="77874-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="77874-113">*szdomainname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77874-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77874-114">Die NULL-terminierte Zeichenfolge, die den Namen der Domäne angibt, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="77874-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="77874-115">*szPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77874-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77874-116">Die NULL-terminierte Zeichenfolge, die das Kennwort des Benutzers in der angegebenen Domäne angibt.</span><span class="sxs-lookup"><span data-stu-id="77874-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77874-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77874-117">Return value</span></span>

<span data-ttu-id="77874-118">Wenn erfolgreich, wird ein Standard- **HRESULT** -Erfolgs Code zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77874-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="77874-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77874-119">Remarks</span></span>

<span data-ttu-id="77874-120">Wenn **dssetauthidentity** nicht aufgerufen wird, wird der Sicherheitskontext des aktuellen Prozesses angenommen.</span><span class="sxs-lookup"><span data-stu-id="77874-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="77874-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77874-121">Requirements</span></span>



| <span data-ttu-id="77874-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77874-122">Requirement</span></span> | <span data-ttu-id="77874-123">Wert</span><span class="sxs-lookup"><span data-stu-id="77874-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77874-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77874-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77874-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77874-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77874-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77874-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77874-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77874-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77874-128">Header</span><span class="sxs-lookup"><span data-stu-id="77874-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="77874-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="77874-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="77874-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77874-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="77874-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77874-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="77874-132">DLL</span><span class="sxs-lookup"><span data-stu-id="77874-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77874-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77874-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="77874-134">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="77874-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77874-135">**Dssetauthidentityw** (Unicode) und **dssetauthidentitya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77874-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="77874-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77874-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77874-137">Sichern und Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="77874-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="77874-138">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="77874-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

