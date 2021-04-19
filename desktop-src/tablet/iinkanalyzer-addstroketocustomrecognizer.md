---
description: Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für einen einzelnen Strich hinzu.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Iinkanalyzer:: addstrokedecustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348794"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Iinkanalyzer:: addstrokedecustomerkenzer-Methode

Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für einen einzelnen Strich hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeid* \[ in\]
</dt> <dd>

Der Bezeichner für den hinzu zufügenden Strich.

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

Die Anzahl der Paket Eigenschaften in jedem Paket.

</dd> <dt>

*pstrokepacketdescriptionguids* \[ in\]
</dt> <dd>

Ein Array, das die Paket Eigenschaften Bezeichner enthält.

</dd> <dt>

*pcustomerkenzer* \[ in\]
</dt> <dd>

Der [**icontextnode**](icontextnode.md) des Typs **customerkenzer** , dem der Strich hinzugefügt werden soll.

</dd> <dt>

*ppcontextnodestrokeaddto* \[ vorgenommen\]
</dt> <dd>

Der [**icontextnode**](icontextnode.md) , dem die Ink-Analyse den Strich hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.

[**Iinkanalyzer**](iinkanalyzer.md) fügt den Strich einem [**icontextnode**](icontextnode.md) des Typs **customerkenzer** hinzu (siehe [Kontext Knoten Typen](context-node-types.md)). Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).

[**Iinkanalyzer**](iinkanalyzer.md) weist den Kultur Bezeichner des aktiven Eingabe Threads dem Strich zu und fügt den Strich dem ersten Knoten **UnclassifiedInk** unter dem Knoten **customerkenzer** hinzu. Wenn kein **unclassimeedink** -Knoten vorhanden ist, wird er erstellt. Wenn das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das dem **customerkenzer** -Knoten zugeordnet ist, den Kultur Bezeichner nicht unterstützt, setzt **iinkanalyzer** die Analyse fort und generiert eine [**ianalysiswarning**](ianalysiswarning.md) -Warnung. Diese Warnung weist einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ LanguageIdNotRespected** auf.

*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich. *pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld des hinzugefügten Strichs erweitert.

Der [**iinkanalyzer**](iinkanalyzer.md) gibt unter den folgenden Umständen ein **HRESULT** von **E \_ invalidArg** zurück.

-   Der [**iinkanalyzer**](iinkanalyzer.md) enthält bereits einen Strich mit dem gleichen Bezeichner wie der hinzu zufügende Strich.
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

[**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: kreatecustomerkenzer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

