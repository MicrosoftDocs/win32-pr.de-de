---
description: Fügt dem IInkAnalyzer Strichdaten für mehrere Striche hinzu und weist den Strichen den angegebenen Kulturbezeichner zu.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: IInkAnalyzer::AddStrokesForLanguage-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 52e2dc742dc91b37bce29d477cf91f7178f2ae2a62ce3a329d2b9bf79c46b33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719608"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>IInkAnalyzer::AddStrokesForLanguage-Methode

Fügt dem [**IInkAnalyzer**](iinkanalyzer.md) Strichdaten für mehrere Striche hinzu und weist den Strichen den angegebenen Kulturbezeichner zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
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

*plIdofStrokesToAdd* \[ In\]
</dt> <dd>

Ein Array, das die Strichbezeichner enthält.

</dd> <dt>

*lStrokesLCID* \[ In\]
</dt> <dd>

Ein -Wert, der den Kulturbezeichner darstellt, der den Strichen zugewiesen werden soll.

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

Der [**IContextNode,**](icontextnode.md) dem das Ink Analyzer die Striche hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodeStrokeAddedTo* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn *ppContextNodeStrokeAddedTo* **NULL ist,** gibt dies an, dass der Aufrufer nicht am Rückgabewert der Methode interessiert ist.

[**IInkAnalyzer fügt**](iinkanalyzer.md) die Striche einem [**IContextNode**](icontextnode.md) vom Typ UnclassifiedInk hinzu (siehe [Kontextknotentypen](context-node-types.md)). Dieser Knoten befindet sich in der Unterknotensammlung des Stammknotens (siehe [**IInkAnalyzer::GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**IContextNode::GetSubNodes-Methoden).**](icontextnode-getsubnodes.md)

Der [**IInkAnalyzer**](iinkanalyzer.md) weist den Strichen den *Kulturbezeichner lStrokeLCID* zu und fügt die Striche dem ersten UnclassifiedInk-Kontextknoten unter dem Stammknoten des Ink Analyzer hinzu, der Striche mit demselben Kulturbezeichner enthält. Wenn das Ink-Analyseprogramm nicht über einen Knoten mit dem gleichen Kulturbezeichner verfügt, erstellt es einen neuen UnclassifiedInk-Kontextknoten unter seinem Stammknoten und fügt die Striche dem neuen UnclassifiedInk-Kontextknoten hinzu.

*plStrokePacketData enthält* Paketdaten für alle Striche. *pStrokePacketDescriptionGuids* enthält die GUIDs (Globally Unique Identifiers), die die Typen von Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine vollständige Liste der verfügbaren Paketeigenschaften finden Sie unter [PacketPropertyGuids-Konstanten.](packetpropertyguids-constants.md)

> [!Note]  
> Nur Striche mit den gleichen Paketbeschreibungen können in einem einzigen Aufruf der [**IInkAnalyzer::AddStrokes-Methode hinzugefügt werden.**](iinkanalyzer-addstrokes.md)

 

Diese Methode erweitert den dirty-Bereich auf die Vereinigung des aktuellen Werts des Region und des Begrenzungsfelds der hinzugefügten Striche.

Wenn [**der IInkAnalyzer**](iinkanalyzer.md) bereits einen Strich mit demselben Bezeichner wie einer der Striche enthält, die hinzugefügt werden sollen, gibt **der IInkAnalyzer** ein **HRESULT** von **E \_ INVALIDARG zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

