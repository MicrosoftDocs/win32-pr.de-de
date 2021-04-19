---
description: Stellt ein Handle für eine installierbare Objekt Bezeichner-Funktion (OID) dar.
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: Hcryptoidfuncaddr (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350386"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="bc3a7-103">Hcryptoidfuncaddr</span><span class="sxs-lookup"><span data-stu-id="bc3a7-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="bc3a7-104">Der **hcryptoidfuncaddr** -Datentyp stellt ein Handle für eine installierbare [*Objekt Bezeichner*](../secgloss/o-gly.md) -Funktion (OID) dar.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="bc3a7-105">Die Funktionen " [**cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)", " [**cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)" und " [**cryptfreoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) " und " [**CERT \_ Store \_ Prov \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) " verwenden diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="bc3a7-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc3a7-106">Requirements</span></span>



| <span data-ttu-id="bc3a7-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc3a7-107">Requirement</span></span> | <span data-ttu-id="bc3a7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bc3a7-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3a7-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc3a7-109">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3a7-110">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc3a7-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bc3a7-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc3a7-111">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3a7-112">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc3a7-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc3a7-113">Header</span><span class="sxs-lookup"><span data-stu-id="bc3a7-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc3a7-114"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3a7-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
