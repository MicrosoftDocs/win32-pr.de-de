---
description: Stellt ein Handle für einen Satz von installierbaren Funktionen für Objekt Bezeichner (OID) dar.
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: Hcryptoidfuncset (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364138"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="a9b71-103">Hcryptoidfuncset</span><span class="sxs-lookup"><span data-stu-id="a9b71-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="a9b71-104">Der **hcryptoidfuncset** -Datentyp stellt ein Handle für einen Satz von installierbaren Funktionen für [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID) dar.</span><span class="sxs-lookup"><span data-stu-id="a9b71-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="a9b71-105">Die Funktionen " [**cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)", " [**cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)", " [**cryptfreoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)" und " [**cryptinitoidfunctionset**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) " verwenden diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a9b71-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="a9b71-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9b71-106">Requirements</span></span>



| <span data-ttu-id="a9b71-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9b71-107">Requirement</span></span> | <span data-ttu-id="a9b71-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b71-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b71-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9b71-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b71-110">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9b71-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9b71-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9b71-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b71-112">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9b71-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9b71-113">Header</span><span class="sxs-lookup"><span data-stu-id="a9b71-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b71-114"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b71-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
