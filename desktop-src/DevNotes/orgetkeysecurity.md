---
description: Ruft eine Kopie der Sicherheits Beschreibung ab, die den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur schützt.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Orgetkeysecurity-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372644"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="5e45b-103">Orgetkeysecurity-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e45b-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="5e45b-104">Ruft eine Kopie der Sicherheits Beschreibung ab, die den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur schützt.</span><span class="sxs-lookup"><span data-stu-id="5e45b-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e45b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e45b-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="5e45b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e45b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e45b-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e45b-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e45b-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="5e45b-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="5e45b-109">*Securityinformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e45b-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e45b-110">Ein [Sicherheits \_ Informations](../secauthz/security-information.md) Wert, der die angeforderten Sicherheitsinformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="5e45b-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="5e45b-111">*psecuritydescriptor* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="5e45b-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e45b-112">Ein Zeiger auf einen Puffer, der eine Kopie der angeforderten Sicherheits Beschreibung empfängt.</span><span class="sxs-lookup"><span data-stu-id="5e45b-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="5e45b-113">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="5e45b-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5e45b-114">*lpcbsecuritydescriptor* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5e45b-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e45b-115">Ein Zeiger auf eine Variable, die die Größe des Puffers in Bytes angibt, auf den der *psecuritydescriptor* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="5e45b-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="5e45b-116">Wenn die Funktion zurückgibt, enthält die Variable die Anzahl der in den Puffer geschriebenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="5e45b-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e45b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e45b-117">Return value</span></span>

<span data-ttu-id="5e45b-118">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den Fehler \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="5e45b-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5e45b-119">Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich NULL zurückgegeben, der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5e45b-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="5e45b-120">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e45b-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="5e45b-121">Wenn der durch den *psecuritydescriptor* -Parameter angegebene Puffer zu klein ist, gibt die Funktion Fehler \_ unzureichenden Puffer zurück, \_ und der *lpcbsecuritydescriptor* -Parameter enthält die Anzahl der Bytes, die für die angeforderte Sicherheits Beschreibung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e45b-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e45b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e45b-122">Requirements</span></span>



| <span data-ttu-id="5e45b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e45b-123">Requirement</span></span> | <span data-ttu-id="5e45b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5e45b-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e45b-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5e45b-125">Redistributable</span></span><br/> | <span data-ttu-id="5e45b-126">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5e45b-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="5e45b-127">Header</span><span class="sxs-lookup"><span data-stu-id="5e45b-127">Header</span></span><br/>          | <dl> <span data-ttu-id="5e45b-128"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e45b-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e45b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5e45b-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="5e45b-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e45b-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e45b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e45b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e45b-132">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="5e45b-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="5e45b-133">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="5e45b-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="5e45b-134">**Orsetkeysecurity**</span><span class="sxs-lookup"><span data-stu-id="5e45b-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="5e45b-135">Sicherheits \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="5e45b-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
