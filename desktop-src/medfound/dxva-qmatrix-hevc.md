---
description: Definiert eine Quantisierungsmatrix.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC -Struktur (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 5d71b392d41c123eb0106d08f1a75d2a5147977b106c811e0bf0786ab2acff2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974589"
---
# <a name="dxva_qmatrix_hevc-structure"></a>DXVA \_ Qmatrix \_ HEVC-Struktur

Definiert eine Quantisierungsmatrix.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a>Member

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

Enthält die Skalierungslisten für den 4x4-Skalierungsprozess, die ScalingList \[ 0 \] \[ MatrixID i in der HEVC-Spezifikation entsprechen, wobei MatrixID im Bereich von 0 bis 5 liegt ( einschließlich) und i im Bereich von 0 bis \] \[ \] 15 liegt (einschließlich).

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungslisten für den 8x8-Skalierungsprozess, die scalingList \[ 1 \] \[ MatrixID i in der HEVC-Spezifikation entsprechen, wobei MatrixID im Bereich von 0 bis 5 liegt ( einschließlich) und i im Bereich von 0 bis \] \[ \] 63 liegt (einschließlich).

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungslisten für den 8x8-Skalierungsprozess, die ScalingList \[ 2 \] \[ MatrixID i in der HEVC-Spezifikation entsprechen, wobei MatrixID im Bereich von 0 bis 5 liegt ( einschließlich) und i im Bereich von 0 bis \] \[ \] 63 liegt (einschließlich).

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungslisten für den 8x8-Skalierungsprozess, die scalingList \[ 3 \] \[ MatrixID i in der HEVC-Spezifikation entsprechen, wobei MatrixID im Bereich von 0 bis 1 liegt ( einschließlich) und i im Bereich von 0 bis \] \[ \] 63 liegt (einschließlich).

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Enthält den DC-Wert der Skalierungsliste für die Größe 16x16 mit sizeID gleich 2 und entspricht der Skalierungsliste \_ \_ dc \_ coef \_ minus8 \[ sizeID − 2 matrixID +8 mit sizeID gleich 2 und matrixID im Bereich von 0 bis \] \[ \] 5 (einschließlich) in der HEVC-Spezifikation.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Enthält den DC-Wert der Skalierungsliste für die Größe 32x32 mit sizeID gleich 3 und entspricht der Skalierungsliste \_ \_ dc \_ coef \_ minus8 \[ sizeID = 2 matrixID +8 mit sizeID gleich 3 und matrixID im Bereich von 0 bis \] \[ \] 1 (einschließlich) in der HEVC-Spezifikation.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Strukturen](media-foundation-structures.md)
</dt> </dl>

 

 




