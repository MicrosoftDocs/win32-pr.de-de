---
description: Fügt dem IInkAnalyzer Strichdaten für mehrere Striche hinzu und weist den Strichen den Kulturbezeichner des aktiven Eingabethreads zu.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: IInkAnalyzer::AddStrokes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed8d58100c2d05b2d87af30cab6d4823df645b53ecb62a5e54a7318ba07743a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939990"
---
# <a name="iinkanalyzeraddstrokes-method"></a>IInkAnalyzer::AddStrokes-Methode

Fügt dem [**IInkAnalyzer**](iinkanalyzer.md) Strichdaten für mehrere Striche hinzu und weist den Strichen den Kulturbezeichner des aktiven Eingabethreads zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der hinzuzufügenden Striche.

</dd> <dt>

*plStrokeIds* \[ In\]
</dt> <dd>

Ein Array, das die Strichbezeichner enthält.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ In\]
</dt> <dd>

Die Anzahl der Eigenschaften in jedem Paket.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ In\]
</dt> <dd>

Ein Array, das die Paketeigenschaftsbezeichner enthält.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ In\]
</dt> <dd>

Ein Array, das die Anzahl der Pakete in jedem Strich enthält.

</dd> <dt>

*plStrokePacketData* \[ In\]
</dt> <dd>

Ein Array, das die Paketdaten für die Striche enthält.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

Der [**IContextNode,**](icontextnode.md) dem das Ink-Analyseprogramm die Striche hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodeStrokeAddedTo* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn *ppContextNodeStrokeAddedTo* **NULL** ist, gibt dies an, dass der Aufrufer nicht an dem Rückgabewert der Methode interessiert ist.

[**IInkAnalyzer**](iinkanalyzer.md) fügt die Striche einem [**IContextNode**](icontextnode.md) des Typs UnclassifiedInk hinzu (siehe [Kontextknotentypen](context-node-types.md)). Dieser Knoten befindet sich in der Unterknotensammlung des Stammknotens (siehe [**IInkAnalyzer::GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**IContextNode::GetSubNodes-Methoden).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) weist den Strichen den Kulturbezeichner des aktiven Eingabethreads zu und fügt die Striche dem ersten UnclassifiedInk-Kontextknoten unter dem Stammknoten des Freihandanalysetools hinzu, der Striche mit dem gleichen Kulturbezeichner enthält. Wenn das Freihandanalyseprogramm keinen Knoten mit demselben Kulturbezeichner hat, erstellt es einen neuen UnclassifiedInk-Kontextknoten unter seinem Stammknoten und fügt die Striche dem neuen UnclassifiedInk-Kontextknoten hinzu.

*plStrokePacketData* enthält Paketdaten für alle Striche. *pStrokePacketDescriptionGuids* enthält die GUIDs (Globally Unique Identifiers), die die Typen von Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine vollständige Liste der verfügbaren Paketeigenschaften finden Sie unter [PacketPropertyGuids-Konstanten.](packetpropertyguids-constants.md)

> [!Note]  
> Nur Striche mit den gleichen Paketbeschreibungen können in einem einzigen Aufruf der **IInkAnalyzer::AddStrokes-Methode** hinzugefügt werden.

 

Diese Methode erweitert den geänderten Bereich auf die Vereinigung des aktuellen Werts der Region und den Begrenzungsfeld der hinzugefügten Striche.

Wenn der [**IInkAnalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Bezeichner wie einer der hinzuzufügenden Striche enthält, gibt **der IInkAnalyzer** ein **HRESULT** von **E \_ INVALIDARG** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

