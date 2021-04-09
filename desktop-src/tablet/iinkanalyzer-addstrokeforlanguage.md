---
description: Fügt dem iinkanalyzer Strich Daten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kultur Bezeichner zu.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'Iinkanalyzer:: addstrokeforlanguage-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862703"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a>Iinkanalyzer:: addstrokeforlanguage-Methode

Fügt dem [**iinkanalyzer**](iinkanalyzer.md) Strich Daten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kultur Bezeichner zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Bezeichner für den hinzu zufügenden Strich.

</dd> <dt>

*lstrokelcid* \[ in\]
</dt> <dd>

Der Kultur Bezeichner, der dem Strich zugewiesen werden soll.

</dd> <dt>

*ulstrokepacketdatacount* \[ in\]
</dt> <dd>

Die Anzahl der Pakete im Strich.

</dd> <dt>

*plstrokepacketdata* \[ in\]
</dt> <dd>

Ein Array, das die Paketdaten für den Strich enthält.

</dd> <dt>

*ulstrokepacketdescriptioncount* \[ in\]
</dt> <dd>

Die Anzahl der Eigenschaften in jedem Paket.

</dd> <dt>

*pstrokepacketdescriptionguids* \[ in\]
</dt> <dd>

Ein Array, das die Paket Eigenschaften Bezeichner enthält.

</dd> <dt>

*ppcontextnodestrokeaddto* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, dessen Wert auf den Zeiger des [**icontextnode**](icontextnode.md) festgelegt ist, der den neu hinzugefügten Strich enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.

[**Iinkanalyzer**](iinkanalyzer.md) fügt den Strich einem [**icontextnode**](icontextnode.md) vom Typ UnclassifiedInk hinzu (siehe [Kontext Knoten Typen](context-node-types.md)). Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).

[**Iinkanalyzer**](iinkanalyzer.md) weist dem Strich den Kultur Bezeichner *lstrokelcid* zu und fügt den Strich dem ersten UnclassifiedInk-Kontext Knoten unter dem Stamm Knoten der Ink Analyzer hinzu, der Striche mit dem gleichen Kultur Bezeichner enthält. Wenn der Ink Analyzer keinen Knoten mit demselben Kultur Bezeichner besitzt, erstellt er einen neuen UnclassifiedInk-Kontext Knoten unter seinem Stamm Knoten und fügt den Strich dem neuen UnclassifiedInk-Kontext Knoten hinzu.

*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich. *pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt im Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld des hinzugefügten Strichs erweitert.

Wenn [**iinkanalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Strich Bezeichner enthält, gibt **iinkanalyzer** ein **HRESULT** von **E \_ invalidArg** zurück.

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

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokesforlanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

