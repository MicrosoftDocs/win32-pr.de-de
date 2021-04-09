---
description: Ruft Analyse Alternativen für die Knoten in einer angegebenen icontextnodes-Sammlung ab.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Iinkanalyzer:: getalternatesforcontextnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129460"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Iinkanalyzer:: getalternatesforcontextnodes-Methode

Ruft Analyse Alternativen für die Knoten in einer angegebenen [**icontextnodes**](icontextnodes.md) -Sammlung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcontextnodes* \[ in\]
</dt> <dd>

Die [**icontextnodes**](icontextnodes.md) -Auflistung, für die die Analyse Alternativen zurückgegeben werden.

</dd> <dt>

*ulmaximumalteraten* \[ in\]
</dt> <dd>

Die maximale Anzahl von Alternativen, die zurückgegeben werden sollen.

</dd> <dt>

*ppalternativen* \[ vorgenommen\]
</dt> <dd>

Das [**ianalysisalterniert**](ianalysisalternates.md) -Objekt, das die Analyse Alternativen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Der oberste [**ianalysisalternate**](ianalysisalternate.md) wird als erste Alternative der Auflistung zurückgegeben.

Die [**icontextnode**](icontextnode.md) -Objekte in *pcontextnodes* müssen keine angrenzenden Bereiche des Dokuments darstellen.

Für jeden Analyse Hinweis in Knoten gibt [**iinkanalyzer**](iinkanalyzer.md) nur die ersten alternativen zurück.

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

[**Iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforstrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

