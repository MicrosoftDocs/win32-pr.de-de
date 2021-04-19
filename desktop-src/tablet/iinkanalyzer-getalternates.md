---
description: Ruft 10 Analyse Alternativen für alle dem iinkanalyzer zugeordneten frei Hand Eingaben ab.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'Iinkanalyzer:: getalteraten-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357350"
---
# <a name="iinkanalyzergetalternates-method"></a>Iinkanalyzer:: getalteraten-Methode

Ruft 10 Analyse Alternativen für alle dem [**iinkanalyzer**](iinkanalyzer.md)zugeordneten frei Hand Eingaben ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppalternativen* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die ersten 10 [**ianalysisalternate**](ianalysisalternate.md) -Objekte für alle frei Hand Eingaben, die mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Die obere Alternative wird als erste Alternative der Auflistung zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Ianalysisalteraten**](ianalysisalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforstrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

