---
description: Legt die Sicherheit eines geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Orsetkeysecurity-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365179"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="2c859-103">Orsetkeysecurity-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c859-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="2c859-104">Legt die Sicherheit eines geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="2c859-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c859-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c859-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="2c859-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c859-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c859-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c859-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="2c859-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2c859-109">*Securityinformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c859-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c859-110">Bitflags, die den Typ der festzulegenden Sicherheitsinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="2c859-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="2c859-111">Dieser Parameter kann eine Kombination der [ \_ Sicherheitsinformations](../secauthz/security-information.md) -Bitflags sein.</span><span class="sxs-lookup"><span data-stu-id="2c859-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="2c859-112">*psecuritydescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c859-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c859-113">Ein Zeiger auf eine [Sicherheits \_ deskriptorstruktur](/windows/win32/api/winnt/ns-winnt-security_descriptor) , die die Sicherheits Attribute angibt, die für den angegebenen Schlüssel festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c859-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c859-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c859-114">Return value</span></span>

<span data-ttu-id="2c859-115">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den Fehler \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="2c859-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2c859-116">Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich NULL zurückgegeben, der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c859-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="2c859-117">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c859-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c859-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c859-118">Requirements</span></span>



| <span data-ttu-id="2c859-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c859-119">Requirement</span></span> | <span data-ttu-id="2c859-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2c859-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c859-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2c859-121">Redistributable</span></span><br/> | <span data-ttu-id="2c859-122">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2c859-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="2c859-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c859-123">Header</span></span><br/>          | <dl> <span data-ttu-id="2c859-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c859-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c859-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c859-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="2c859-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c859-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c859-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c859-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c859-128">**Orclosekey**</span><span class="sxs-lookup"><span data-stu-id="2c859-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="2c859-129">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="2c859-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="2c859-130">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="2c859-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="2c859-131">**Orgetkeysecurity**</span><span class="sxs-lookup"><span data-stu-id="2c859-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="2c859-132">Sicherheits \_ Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c859-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="2c859-133">Sicherheits \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="2c859-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
