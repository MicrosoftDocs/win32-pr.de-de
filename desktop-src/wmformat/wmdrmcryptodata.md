---
title: WMDRMCryptoData-Struktur (Wmdrmsdk.h)
description: Die WMDRMCryptoData-Struktur enthält Informationen über den kryptografischen Algorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- WMDRMCryptoData-Strukturfenster Medienformat
- Strukturfenster Medienformat
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
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083804"
---
# <a name="wmdrmcryptodata-structure"></a>WMDRMCryptoData-Struktur

Die **WMDRMCryptoData-Struktur** enthält Informationen über den kryptografischen Algorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.

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

**cryptoType**
</dt> <dd>

Member der [**DRM \_ CRYPTO \_ TYPE-Enumeration,**](drm-crypto-type.md) der den Typ des kryptografischen Algorithmus angibt.

</dd> <dt>

**qwCounterID**
</dt> <dd>

Die hohen 64 Bits des 128-Bit-AES-Indikatormodus. Dieser Member wird nur verwendet, wenn der **cryptoType-Member** auf **CRYPTO TYPE \_ \_ MCE** festgelegt ist.

</dd> <dt>

**qwOffset**
</dt> <dd>

Die niedrigen 64 Bits des 128-Bit-AES-Indikatormodus. Dieser Member wird nur verwendet, wenn der **cryptoType-Member** auf **CRYPTO TYPE \_ \_ MCE** festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





