---
title: Wmdrmcryptodata-Struktur (wmdrmsdk. h)
description: Die wmdrmcryptodata-Struktur enthält Informationen über den Kryptografiealgorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Wmdrmcryptodata-Struktur Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371452"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="dffe4-105">Wmdrmcryptodata-Struktur</span><span class="sxs-lookup"><span data-stu-id="dffe4-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="dffe4-106">Die **wmdrmcryptodata** -Struktur enthält Informationen über den Kryptografiealgorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dffe4-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffe4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dffe4-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="dffe4-108">Member</span><span class="sxs-lookup"><span data-stu-id="dffe4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dffe4-109">**cryptotype**</span><span class="sxs-lookup"><span data-stu-id="dffe4-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="dffe4-110">Member der DRM-kryptografietyp-Enumeration, die den Typ des kryptografischen Algorithmus angibt. [**\_ \_**](drm-crypto-type.md)</span><span class="sxs-lookup"><span data-stu-id="dffe4-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="dffe4-111">**qwcounterid**</span><span class="sxs-lookup"><span data-stu-id="dffe4-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="dffe4-112">Die hohen 64 Bits des 128-Bit-AES-Counter-Modus.</span><span class="sxs-lookup"><span data-stu-id="dffe4-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="dffe4-113">Dieser Member wird nur verwendet, wenn der **cryptotype** -Member auf den **kryptografietyp \_ \_ MCE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dffe4-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="dffe4-114">**qwoffset**</span><span class="sxs-lookup"><span data-stu-id="dffe4-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="dffe4-115">Die unteren 64 Bits des 128-Bit-AES-Counter-Modus.</span><span class="sxs-lookup"><span data-stu-id="dffe4-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="dffe4-116">Dieser Member wird nur verwendet, wenn der **cryptotype** -Member auf den **kryptografietyp \_ \_ MCE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dffe4-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dffe4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dffe4-117">Requirements</span></span>



| <span data-ttu-id="dffe4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dffe4-118">Requirement</span></span> | <span data-ttu-id="dffe4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dffe4-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dffe4-120">Header</span><span class="sxs-lookup"><span data-stu-id="dffe4-120">Header</span></span><br/> | <dl> <span data-ttu-id="dffe4-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dffe4-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffe4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dffe4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffe4-123">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="dffe4-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





