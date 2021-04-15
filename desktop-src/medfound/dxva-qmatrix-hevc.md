---
description: Definiert eine quantisierungsmatrix.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC-Struktur (DXVA. h)
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
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524547"
---
# <a name="dxva_qmatrix_hevc-structure"></a>DXVA- \_ QMatrix \_ hevc-Struktur

Definiert eine quantisierungsmatrix.

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

Enthält die Skalierungs Listen für den 4 x 4-Skalierungs Prozess entsprechend der skinglist \[ 0 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 15 (einschließlich).

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 1 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 63 (einschließlich).

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 2 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 63 (einschließlich).

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 3 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich zwischen 0 und 1 (einschließlich) liegt. der Bereich liegt zwischen 0 und 63 (einschließlich).

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Enthält den DC-Wert der Skalierungs Liste für die 16x16-Größe mit der sizeid gleich 2 und entspricht der Skalierungs \_ Liste \_ DC \_ coef \_ Minus8 \[ sizeid − 2 \] \[ MatrixID \] + 8 mit sizeid ist gleich 2 und MatrixID im Bereich von 0 bis 5 (einschließlich) in der hevc-Spezifikation.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Enthält den DC-Wert der Skalierungs Liste für die Größe 32x32 mit sizeid gleich 3 und entspricht dem Skalierungs \_ Listen- \_ DC \_ coef \_ Minus8 \[ sizeid − 2 \] \[ MatrixID \] + 8 mit sizeid, gleich 3 und MatrixID im Bereich von 0 bis 1 (einschließlich) in der hevc-Spezifikation.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Strukturen](media-foundation-structures.md)
</dt> </dl>

 

 




