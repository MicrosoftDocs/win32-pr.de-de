---
description: Ruft die icontextnode-Objekte ab, die mit dieser alternativen verknüpft sind.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Ianalysisalternate:: getalternatenodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345741"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Ianalysisalternate:: getalternatenodes-Methode

Ruft die [**icontextnode**](icontextnode.md) -Objekte ab, die mit dieser alternativen verknüpft sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppalternative enodes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die [**icontextnode**](icontextnode.md) -Objekte enthält, die mit dieser alternativen verknüpft sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternativen enodes* , wenn Sie die Auflistung der Kontext Knoten nicht mehr verwenden müssen.

 

Diese Methode gibt die Blatt Kontext Knoten zurück, die dieser alternativen zugeordnet sind. Beispiele für Blattknoten sind InkWord-, textword-, Bild-, InkDrawing-und InkBullet-Kontext Knoten. Weitere Informationen finden Sie unter [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md).

Da Sie mit alternativen übereinstimmen, sind diese [**icontextnode**](icontextnode.md) -Objekte keine Nachfolger des Stamm- **icontextnode** des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)), es sei denn, Sie sind die obere Alternative, d. h. das erste Element in einer [**ianalysisalterors**](ianalysisalternates.md) -Auflistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnodes**](icontextnodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> <dt>

[System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. Alternativen](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

