---
description: Aktualisiert die Paketdaten für die angegebenen Striche.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Iinkanalyzer:: UpdateStrokesData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343690"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>Iinkanalyzer:: UpdateStrokesData-Methode

Aktualisiert die Paketdaten für die angegebenen Striche.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der zu aktualisierenden Striche.

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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

der *plstrokepacketdata* -Parameter enthält Paketdaten für alle Striche. Der *pstrokepacketdescriptionguids* -Parameter enthält die Global Unique Identifier (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen **iinkanalyzer:: UpdateStrokesData-Methode** aktualisiert werden.

Mit dieser Methode wird der geänderte Bereich der Ink Analyzer nicht aktualisiert (Weitere Informationen finden Sie unter [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Wenn ein angegebener Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.

Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.

Diese Methode gibt einen Fehlercode zurück, wenn *plstrokeids* **null** ist.

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

[**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokesforlanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: ClearStrokeData-Methode**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_Ianalysil Vents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




