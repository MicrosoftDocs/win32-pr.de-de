---
description: Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für mehrere Striche hinzu.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Iinkanalyzer:: addstrokestocustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347780"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>Iinkanalyzer:: addstrokestocustomerkenzer-Methode

Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für mehrere Striche hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der hinzu zufügenden Striche.

</dd> <dt>

*plstrokeids* \[ in\]
</dt> <dd>

Ein Array, das die Strich Bezeichner enthält.

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

*pcustomerkenzer* \[ in\]
</dt> <dd>

Der [**icontextnode**](icontextnode.md) des Typs **customerkenzer** , dem die Striche hinzugefügt werden sollen.

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

Der [**iinkanalyzer**](iinkanalyzer.md) fügt die Striche einem [**icontextnode**](icontextnode.md) des Typs **customerkenzer** hinzu (siehe [Kontext Knoten Typen](context-node-types.md)). Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).

[**Iinkanalyzer**](iinkanalyzer.md) weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu und fügt die Striche dem ersten Knoten **unclassimeedink** unter dem Knoten **customerkenzer** hinzu. Wenn kein **unclassimeedink** -Knoten vorhanden ist, wird er erstellt. Wenn das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das dem **customerkenzer** -Knoten zugeordnet ist, den Kultur Bezeichner nicht unterstützt, setzt **iinkanalyzer** die Analyse fort und generiert eine [**ianalysiswarning**](ianalysiswarning.md) -Warnung. Diese Warnung weist einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ LanguageIdNotRespected** auf.

*plstrokepacketdata* enthält Paketdaten für alle Striche. *pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

> [!Note]  
> Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen **iinkanalyzer:: addstrokestocustomerkenzer-Methoden** aufgerufen werden.

 

Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld der hinzugefügten Striche erweitert.

Der [**iinkanalyzer**](iinkanalyzer.md) gibt unter den folgenden Umständen ein **HRESULT** von **E \_ invalidArg** zurück.

-   Der [**iinkanalyzer**](iinkanalyzer.md) enthält bereits einen Strich mit dem gleichen Bezeichner wie einen der hinzu zufügenden Striche.
-   Der *pcustomerkenzer* -Parameter enthält einen benutzerdefinierten Erkennungs Knoten, der mit einem anderen [**iinkanalyzer**](iinkanalyzer.md) -Objekt verknüpft ist.
-   Der *pcustomerkenzer* -Parameter enthält einen [**icontextnode**](icontextnode.md) , der nicht vom Typ " **customerkenzer**" ist.

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

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: kreatecustomerkenzer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

