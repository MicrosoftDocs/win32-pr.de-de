---
title: Facteritem. getdataat-Methode
description: Ruft den angegebenen Leistungs Zählers von einem bestimmten Punkt im Diagramm ab.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Getdataat-Methode (Sysmon)
- Getdataat-Methode "sysmon", "ratteritem"-Objekt
- Inititeritem-Objekt (Sysmon), getdataat-Methode
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517921"
---
# <a name="counteritemgetdataat-method"></a>Facteritem. getdataat-Methode

Ruft den angegebenen Leistungs Zählers von einem bestimmten Punkt im Diagramm ab.

## <a name="syntax"></a>Syntax


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

NULL basierter Index des Diagramm Punkts, dessen Wert abgerufen werden soll. Gültige Werte liegen im Bereich von 0 bis ([**Systemmonitor. datapointcount**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*welches* \[ in\]
</dt> <dd>

Der Typ des abzurufenden Leistungs Zählers, z. b. der durchschnittliche Wert des Zählers, der im Diagramm Fenster angezeigt wird. Mögliche Werte finden Sie unter [**sysmondatatype**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*Variant* \[ vorgenommen\]
</dt> <dd>

Der abgerufene Wert des Leistungs Zählers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode nur, wenn

-   [**Systemmonitor. Display Type**](systemmonitor-displaytype.md) ist auf sysmonlinegraph festgelegt.
-   [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) ist auf sysmonlogfiles oder sysmonsqllog festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> <dt>

[**"Count. getstatistics"**](counteritem-getstatistics.md)
</dt> <dt>

[**"Count. GetValue"**](counteritem-getvalue.md)
</dt> </dl>

 

 





