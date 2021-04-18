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
# <a name="wmdrmcryptodata-structure"></a>Wmdrmcryptodata-Struktur

Die **wmdrmcryptodata** -Struktur enthält Informationen über den Kryptografiealgorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**cryptotype**
</dt> <dd>

Member der DRM-kryptografietyp-Enumeration, die den Typ des kryptografischen Algorithmus angibt. [**\_ \_**](drm-crypto-type.md)

</dd> <dt>

**qwcounterid**
</dt> <dd>

Die hohen 64 Bits des 128-Bit-AES-Counter-Modus. Dieser Member wird nur verwendet, wenn der **cryptotype** -Member auf den **kryptografietyp \_ \_ MCE** festgelegt ist.

</dd> <dt>

**qwoffset**
</dt> <dd>

Die unteren 64 Bits des 128-Bit-AES-Counter-Modus. Dieser Member wird nur verwendet, wenn der **cryptotype** -Member auf den **kryptografietyp \_ \_ MCE** festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





