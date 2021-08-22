---
title: WMDRM_ENCRYPT_SCATTER_INFO -Struktur (Wmdrmsdk.h)
description: Die WMDRM ENCRYPT SCATTER INFO-Struktur enthält Informationen, die zum Konfigurieren der \_ \_ \_ IWMDRMEncryptScatter-Schnittstelle für die Verwendung erforderlich sind.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef766f40742713b01648348bedb4c1a35494fdc02d02843f8f2a41f133938a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083814"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>WMDRM \_ ENCRYPT \_ SCATTER \_ INFO-Struktur

Die **WMDRM \_ ENCRYPT SCATTER \_ \_ INFO-Struktur** enthält Informationen, die zum Konfigurieren der [**IWMDRMEncryptScatter-Schnittstelle**](iwmdrmencryptscatter.md) für die Verwendung erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwStreamID**
</dt> <dd>

Bezeichner des zu verschlüsselnden Streams.

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

Beispielschutzversion, die zum Codieren von Daten aus dem angegebenen Stream verwendet werden soll.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Größe des **pbProtectionInfo-Puffers** in Bytes.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Puffer mit zusätzlichen Schutzinformationen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von der [**IWMDRMEncryptScatter::InitEncryptScatter-Methode**](iwmdrmencryptscatter-initencryptscatter.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





