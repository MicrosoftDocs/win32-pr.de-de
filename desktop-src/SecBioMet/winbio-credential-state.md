---
title: WINBIO_CREDENTIAL_STATE-Enumeration (winbio \_ types. h)
description: Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmelde Informationen zugeordnet wurden.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE Enumeration Windows-Biometrieframework-API
- PWINBIO_CREDENTIAL_STATE enumerationszeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340427"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="a144f-105">Winbio \_ Credential \_ State-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a144f-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="a144f-106">Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmelde Informationen zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="a144f-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="a144f-107">Diese Enumeration wird von der [**winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="a144f-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a144f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a144f-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="a144f-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a144f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a144f-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**winbio-Anmelde Informationen \_ \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="a144f-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="a144f-111">Dem Endbenutzer wurden Anmelde Informationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a144f-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="a144f-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**winbio-Anmelde Informationen \_ \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="a144f-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="a144f-113">Dem Endbenutzer wurden keine Anmelde Informationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a144f-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a144f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a144f-114">Requirements</span></span>



| <span data-ttu-id="a144f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a144f-115">Requirement</span></span> | <span data-ttu-id="a144f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a144f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a144f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a144f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a144f-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a144f-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a144f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a144f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a144f-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a144f-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a144f-121">Header</span><span class="sxs-lookup"><span data-stu-id="a144f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a144f-122"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a144f-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a144f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a144f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a144f-124">Enumerationen von Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a144f-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a144f-125">**Winbiogetkredentialstate**</span><span class="sxs-lookup"><span data-stu-id="a144f-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





