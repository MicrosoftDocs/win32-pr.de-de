---
description: Ruft das umgebende Rechteck des ianalysisregion-Elements ab.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Ianalysisregion:: GetBounds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751873"
---
# <a name="ianalysisregiongetbounds-method"></a>Ianalysisregion:: GetBounds-Methode

Ruft das umgebende Rechteck des [**ianalysisregion**](ianalysisregion.md)-Elements ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pboundingrechteck* \[ vorgenommen\]
</dt> <dd>

Das umgebende Rechteck von [**ianalysisregion**](ianalysisregion.md) in frei Hand Raumkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Die Begrenzungen befinden sich in frei Hand Raumkoordinaten.

Wenn [**ianalysisregion**](ianalysisregion.md) einen unendlichen Bereich darstellt, sind die linken und oberen Begrenzungen **int \_ Min**, und die Rechte und unteren Begrenzungen sind **int \_ Max**.

Wenn [**ianalysisregion**](ianalysisregion.md) einen leeren Bereich darstellt, sind alle Begrenzungen des Rechtecks 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Ianalysisregion:: GetRegionScans-Methode**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




