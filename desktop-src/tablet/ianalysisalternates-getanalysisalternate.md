---
description: Ruft das ianalysisalternate-Objekt am angegebenen Index in der Collection ab.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Ianalysisalterors:: getanalysisalternate-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344464"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>Ianalysisalternate:: getanalysisalternate-Methode

Ruft das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Collection ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulindex* \[ in\]
</dt> <dd>

Der null basierte Index des abzurufenden [**ianalysisalternate**](ianalysisalternate.md) -Objekts.

</dd> <dt>

*ppalternate* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Auflistung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternate* , wenn Sie die Alternative Analyse nicht mehr verwenden müssen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalteraten**](ianalysisalternates.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

