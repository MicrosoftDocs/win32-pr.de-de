---
title: WINBIO_CREDENTIAL_FORMAT-Enumeration (winbio \_ types. h)
description: Definiert Flags, die verwendet werden können, um das Format der Anmelde Informationen für den Endbenutzer anzugeben.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT Enumeration Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103695"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="237fa-104">Winbio \_ Credential \_ Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="237fa-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="237fa-105">Definiert Flags, die verwendet werden können, um das Format der Anmelde Informationen für den Endbenutzer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="237fa-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="237fa-106">Diese Enumeration wird von der [**winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="237fa-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="237fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="237fa-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="237fa-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="237fa-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="237fa-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**winbio- \_ Kennwort \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="237fa-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="237fa-110">Das Kennwort ist in einem generischen Format angegeben.</span><span class="sxs-lookup"><span data-stu-id="237fa-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="237fa-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**winbio- \_ Kennwort \_ gepackt**</span><span class="sxs-lookup"><span data-stu-id="237fa-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="237fa-112">Das Kennwort weist ein komprimiertes Format auf.</span><span class="sxs-lookup"><span data-stu-id="237fa-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="237fa-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**winbio- \_ Kennwort \_ geschützt**</span><span class="sxs-lookup"><span data-stu-id="237fa-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="237fa-114">Die Kenn Wort Anmelde Informationen wurden mit " [**kredprotect**](/windows/desktop/api/wincred/nf-wincred-credprotecta)" umschließt.</span><span class="sxs-lookup"><span data-stu-id="237fa-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="237fa-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="237fa-115">Requirements</span></span>



| <span data-ttu-id="237fa-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="237fa-116">Requirement</span></span> | <span data-ttu-id="237fa-117">Wert</span><span class="sxs-lookup"><span data-stu-id="237fa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="237fa-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="237fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="237fa-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="237fa-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="237fa-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="237fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="237fa-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="237fa-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="237fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="237fa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="237fa-123"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="237fa-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="237fa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="237fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237fa-125">Enumerationen von Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="237fa-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="237fa-126">**Winbiosetcredential**</span><span class="sxs-lookup"><span data-stu-id="237fa-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

