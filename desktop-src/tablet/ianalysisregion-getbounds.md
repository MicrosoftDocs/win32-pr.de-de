---
description: Ruft das umgebundene Rechteck von IAnalysisRegion ab.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: IAnalysisRegion::GetBounds-Methode (IACom.h)
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
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092331"
---
# <a name="ianalysisregiongetbounds-method"></a>IAnalysisRegion::GetBounds-Methode

Ruft das umgebundene Rechteck der [**IAnalysisRegion ab.**](ianalysisregion.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBoundingRectangle* \[ out\]
</dt> <dd>

Das umgebundene Rechteck der [**IAnalysisRegion**](ianalysisregion.md) in Freiraumkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Die Begrenzungen befinden sich in Freiraumkoordinaten.

Wenn [**IAnalysisRegion**](ianalysisregion.md) einen unendlichen Bereich darstellt, sind die linke und die obere Grenze **INT \_ MIN,** und die rechte und die untere Grenze sind **INT \_ MAX.**

Wenn [**IAnalysisRegion einen**](ianalysisregion.md) leeren Bereich darstellt, sind alle Begrenzungen des Rechtecks 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::GetRegionScans-Methode**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




