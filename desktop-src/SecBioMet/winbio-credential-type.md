---
title: WINBIO_CREDENTIAL_TYPE-Enumeration (winbio \_ types. h)
description: Definiert Flags, die verwendet werden können, um nach dem Anmelde Informationstyp zu filtern.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE Enumeration Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859268"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="873bd-104">Winbio \_ Credential \_ Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="873bd-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="873bd-105">Definiert Flags, die verwendet werden können, um nach dem Anmelde Informationstyp zu filtern.</span><span class="sxs-lookup"><span data-stu-id="873bd-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="873bd-106">Diese Enumeration wird von den Funktionen " [**winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)", " [**winbioremovecredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)" und " [**winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="873bd-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="873bd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="873bd-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="873bd-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="873bd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="873bd-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**Kennwort für winbio-Anmelde Informationen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="873bd-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="873bd-110">Filtert Kenn Wort Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="873bd-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="873bd-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**winbio \_ Credential \_ all**</span><span class="sxs-lookup"><span data-stu-id="873bd-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="873bd-112">Filtert alle Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="873bd-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="873bd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="873bd-113">Requirements</span></span>



| <span data-ttu-id="873bd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="873bd-114">Requirement</span></span> | <span data-ttu-id="873bd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="873bd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873bd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="873bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="873bd-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="873bd-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="873bd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="873bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="873bd-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="873bd-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="873bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="873bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="873bd-121"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="873bd-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873bd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="873bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873bd-123">Enumerationen von Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="873bd-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="873bd-124">**Winbiogetkredentialstate**</span><span class="sxs-lookup"><span data-stu-id="873bd-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="873bd-125">**Winbioremovecredential**</span><span class="sxs-lookup"><span data-stu-id="873bd-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="873bd-126">**Winbiosetcredential**</span><span class="sxs-lookup"><span data-stu-id="873bd-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





