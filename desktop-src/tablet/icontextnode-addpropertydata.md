---
description: Fügt eine bestimmte anwendungsspezifische Daten hinzu.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Icontextnode:: AddPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129508"
---
# <a name="icontextnodeaddpropertydata-method"></a>Icontextnode:: AddPropertyData-Methode

Fügt eine bestimmte anwendungsspezifische Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppropertydataid* \[ in\]
</dt> <dd>

Eine Globally Unique Identifier (GUID), die zum Identifizieren des Datentyps verwendet wird.

</dd> <dt>

*ulpropertydatasize* \[ in\]
</dt> <dd>

Die Größe der Daten in Bytes.

</dd> <dt>

*pbpropertiesdata* \[ in\]
</dt> <dd>

\[in ist size \_ (ulpropertydatasize)\]

Ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die hinzu zufügenden Eigenschaften Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **icontextnode:: AddPropertyData** zum Zuordnen von Daten zu einem Kontext Knoten. Um die Daten zu einem späteren Zeitpunkt abzurufen, verwenden Sie [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md).

Der Ink Analyzer kann den Knoten als Teil der frei Hand Analyse löschen, es sei denn, der Kontext Knoten ist bestätigt (siehe [**icontextnode:: Confirm**](icontextnode-confirm.md)). Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Icontextnode:: loadpropertiesdata**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




