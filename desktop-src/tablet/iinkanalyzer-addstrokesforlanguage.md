---
description: Fügt dem iinkanalyzer Strich Daten für mehrere Striche hinzu und weist den Strichen den angegebenen Kultur Bezeichner zu.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'Iinkanalyzer:: addstrokesforlanguage-Methode (iacom. h)'
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
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214667"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>Iinkanalyzer:: addstrokesforlanguage-Methode

Fügt dem [**iinkanalyzer**](iinkanalyzer.md) Strich Daten für mehrere Striche hinzu und weist den Strichen den angegebenen Kultur Bezeichner zu.

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

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der hinzu zufügenden Striche.

</dd> <dt>

*plidof strokesToAdd* \[ in\]
</dt> <dd>

Ein Array, das die Strich Bezeichner enthält.

</dd> <dt>

*lstrokeslcid* \[ in\]
</dt> <dd>

Ein-Wert, der den Kultur Bezeichner darstellt, der den Strichen zugewiesen werden soll.

</dd> <dt>

*ulstrokepacketdescriptioncount* \[ in\]
</dt> <dd>

Die Anzahl der Eigenschaften in jedem Paket.

</dd> <dt>

*pstrokepacketdescriptionguids* \[ in\]
</dt> <dd>

Ein Array, das die Paket Eigenschaften Bezeichner enthält.

</dd> <dt>

*pulpacketdatacountperstroke* \[ in\]
</dt> <dd>

Ein Array, das die Anzahl der Pakete in jedem Strich enthält.

</dd> <dt>

*plstrokepacketdata* \[ in\]
</dt> <dd>

Ein Array, das die Paketdaten für die Striche enthält.

</dd> <dt>

*ppcontextnodestrokeaddto* \[ vorgenommen\]
</dt> <dd>

Der [**icontextnode**](icontextnode.md) , dem die Handschrift Analyse die Striche hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.

Der [**iinkanalyzer**](iinkanalyzer.md) fügt die Striche einem [**icontextnode**](icontextnode.md) vom Typ unclassimeedink hinzu (siehe [Kontext Knoten Typen](context-node-types.md)). Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).

Der [**iinkanalyzer**](iinkanalyzer.md) weist den Strichen den Kultur Bezeichner " *lstrokelcid* " zu und fügt die Striche dem ersten unclassi\edink-Kontext Knoten unter dem Stamm Knoten der Ink Analyzer hinzu, der Striche mit dem gleichen Kultur Bezeichner enthält. Wenn der Ink Analyzer keinen Knoten mit demselben Kultur Bezeichner besitzt, erstellt er einen neuen unclassimeedink-Kontext Knoten unter seinem Stamm Knoten und fügt die Striche dem neuen unclassi\edink-Kontext Knoten hinzu.

*plstrokepacketdata* enthält Paketdaten für alle Striche. *pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

> [!Note]  
> Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen [**iinkanalyzer:: AddStrokes-Methoden**](iinkanalyzer-addstrokes.md)aufgerufen werden.

 

Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld der hinzugefügten Striche erweitert.

Wenn [**iinkanalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Bezeichner wie einen der hinzu zufügenden Striche enthält, gibt **iinkanalyzer** ein **HRESULT** von **E \_ invalidArg** zurück.

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

[**Iinkanalyzer:: AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

