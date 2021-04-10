---
description: Erstellt einen neuen benutzerdefinierten Erkennungs Knoten für iinkanalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Iinkanalyzer:: kreatecustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214665"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>Iinkanalyzer:: kreatecustomerkenzer-Methode

Erstellt einen neuen benutzerdefinierten Erkennungs Knoten für [**iinkanalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalysiserkenzerid* \[ in\]
</dt> <dd>

Die Globally Unique Identifier (GUID) des [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Elements, für das ein Knoten erstellt werden soll.

</dd> <dt>

*ppcontextnode* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das den neuen benutzerdefinierten Erkennungs Knoten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf ppcontextnode, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Diese Methode erstellt einen neuen [**icontextnode**](icontextnode.md) mit dem Typ customerkenzer (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)). Anschließend wird der neue benutzerdefinierte Erkennungs Knoten der subknotenauflistung des Stamm Knotens des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzugefügt (Weitere Informationen finden Sie unter [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).

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

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

