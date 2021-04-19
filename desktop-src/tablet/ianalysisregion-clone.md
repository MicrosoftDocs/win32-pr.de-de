---
description: Erstellt eine Kopie von ianalysisregion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Ianalysisregion:: Clone-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348796"
---
# <a name="ianalysisregionclone-method"></a>Ianalysisregion:: Clone-Methode

Erstellt eine Kopie von [**ianalysisregion**](ianalysisregion.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclonedregion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Kopie von [**ianalysisregion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Diese Methode ist eqivalente in die Thesystem. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone-Methode im .NET Framework.

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) in \* *pclonedregion* aufrufen, wenn Sie den geklonten Analysebereich nicht mehr verwenden müssen.

 

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

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

