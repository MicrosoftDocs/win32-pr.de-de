---
description: Wird als Handle für einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) oder CNG-CSP von CryptoAPI verwendet.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352628"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="ba6b0-103">hcryptprov- \_ oder \_ NCrypt- \_ Schlüssel \_ handle</span><span class="sxs-lookup"><span data-stu-id="ba6b0-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="ba6b0-104">Der Datentyp " **hcryptprov" \_ oder " \_ NCrypt \_ Key \_ handle** " wird als Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) oder CNG-CSP verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba6b0-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="ba6b0-105">Dieses Handle muss ein [**hcryptprov**](hcryptprov.md) -Handle sein, das mithilfe der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion oder eines **NCrypt- \_ Schlüssel \_ handle** -Handles erstellt wurde, der mit der [**ncryptopenkey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba6b0-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="ba6b0-106">Neue Anwendungen sollten immer das **NCrypt- \_ Schlüssel \_ handle** an einen CNG-CSP übergeben.</span><span class="sxs-lookup"><span data-stu-id="ba6b0-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="ba6b0-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba6b0-107">Requirements</span></span>



| <span data-ttu-id="ba6b0-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba6b0-108">Requirement</span></span> | <span data-ttu-id="ba6b0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ba6b0-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6b0-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba6b0-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ba6b0-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba6b0-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba6b0-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba6b0-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ba6b0-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba6b0-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba6b0-114">Header</span><span class="sxs-lookup"><span data-stu-id="ba6b0-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba6b0-115"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba6b0-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
