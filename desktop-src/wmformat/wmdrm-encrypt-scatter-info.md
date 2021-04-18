---
title: WMDRM_ENCRYPT_SCATTER_INFO Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Verschlüsselungs Punkt \_ \_ Info Struktur enthält Informationen, die erforderlich sind, um die zu verwendende iwmdrmencryptscatter-Schnittstelle zu konfigurieren.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364892"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>WMDRM- \_ Verschlüsselungs Punkt \_ Info- \_ Struktur

Die **WMDRM- \_ Verschlüsselungs Punkt \_ \_ Info** Struktur enthält Informationen, die erforderlich sind, um die zu verwendende [**iwmdrmencryptscatter**](iwmdrmencryptscatter.md) -Schnittstelle zu konfigurieren.

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

**dwstreamid**
</dt> <dd>

Der Bezeichner des zu verschlüsselnden Streams.

</dd> <dt>

**dwsampleschutzversion**
</dt> <dd>

Die Beispiel Schutz Version, die zum Codieren von Daten aus dem angegebenen Stream verwendet werden soll.

</dd> <dt>

**cbschutzinfo**
</dt> <dd>

Größe des **pbschutzinfo** -Puffers in Bytes.

</dd> <dt>

**pbschutzinfo**
</dt> <dd>

Puffer mit zusätzlichen Schutz Informationen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von der [**iwmdrmencryptscatter:: initencryptscatter**](iwmdrmencryptscatter-initencryptscatter.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





