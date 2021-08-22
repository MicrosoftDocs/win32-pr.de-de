---
description: Fügt dem IInkAnalyzer Strichdaten für einen einzelnen Strich hinzu und weist dem Strich den Kulturbezeichner des aktiven Eingabethreads zu.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: IInkAnalyzer::AddStroke-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590590"
---
# <a name="iinkanalyzeraddstroke-method"></a>IInkAnalyzer::AddStroke-Methode

Fügt dem [**IInkAnalyzer**](iinkanalyzer.md) Strichdaten für einen einzelnen Strich hinzu und weist dem Strich den Kulturbezeichner des aktiven Eingabethreads zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Bezeichner für den hinzuzufügenden Strich.

</dd> <dt>

*ulStrokePacketDataCount* \[ In\]
</dt> <dd>

Die Anzahl der Pakete im Strich.

</dd> <dt>

*plStrokePacketData* \[ In\]
</dt> <dd>

Ein Array, das die Paketdaten für den Strich enthält.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ In\]
</dt> <dd>

Die Anzahl der Paketeigenschaften in jedem Paket.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ In\]
</dt> <dd>

Ein Array, das die Paketeigenschaftsbezeichner enthält.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

Ein Zeiger auf den [**IContextNode,**](icontextnode.md) dem der [**IInkAnalyzer**](iinkanalyzer.md) den Strich hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodeStrokeAddedTo* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn *ppContextNodeStrokeAddedTo* **NULL** ist, gibt dies an, dass der Aufrufer nicht an dem Rückgabewert der Methode interessiert ist.

Der [**IInkAnalyzer**](iinkanalyzer.md) fügt den Strich einem [**IContextNode**](icontextnode.md) vom Typ UnclassifiedInk hinzu (siehe [Kontextknotentypen](context-node-types.md)). Dieser Knoten befindet sich in der Unterknotensammlung des Stammknotens (siehe [**IInkAnalyzer::GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**IContextNode::GetSubNodes-Methoden).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) weist dem Strich den Kulturbezeichner des aktiven Eingabethreads zu und fügt den Strich dem ersten UnclassifiedInk-Kontextknoten unter dem Stammknoten des Freihandanalysetools hinzu, der Striche mit dem gleichen Kulturbezeichner enthält. Wenn das Freihandanalyseprogramm keinen Knoten mit demselben Kulturbezeichner hat, erstellt er einen neuen UnclassifiedInk-Kontextknoten unter seinem Stammknoten und fügt den Strich dem neuen UnclassifiedInk-Kontextknoten hinzu.

*plStrokePacketData* enthält Paketdaten für alle Punkte im Strich. *pStrokePacketDescriptionGuids* enthält die GUIDs (Globally Unique Identifiers), die die Paketdatentypen beschreiben, die für jeden Punkt im Strich enthalten sind. Eine vollständige Liste der verfügbaren Paketeigenschaften finden Sie unter [PacketPropertyGuids-Konstanten.](packetpropertyguids-constants.md)

Diese Methode erweitert den geänderten Bereich auf die Vereinigung des aktuellen Werts des Bereichs und des begrenzungsfelds des hinzugefügten Strichs.

Wenn der [**IInkAnalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Strichbezeichner enthält, gibt **der IInkAnalyzer** ein **HRESULT** von **E \_ INVALIDARG** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

