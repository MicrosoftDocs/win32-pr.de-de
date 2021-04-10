---
title: System Monitor DataSourceType (Eigenschaft)
description: Ruft die Quelle der Leistungsdaten des Leistungsindikators ab oder legt Sie fest.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- DataSourceType-Eigenschaft (Sysmon)
- DataSourceType-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, DataSourceType (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040823"
---
# <a name="systemmonitordatasourcetype-property"></a>Systemmonitor::D atasourcetype-Eigenschaft

Ruft die Quelle der Leistungsdaten des Leistungsindikators ab oder legt Sie fest.

## <a name="syntax"></a>Syntax


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Eigenschaftswert

Quelle der Leistungsdaten. Mögliche Werte finden Sie unter [**datasourcetypeer Konstanten**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Ausnahmen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ausnahmetyp</th>
<th>Bedingung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System.ArgumentException</strong></td>
<td>Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:
<ul>
<li>Der angegebene Datenquellen Wert ist ungültig.</li>
<li>Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, kann von sysmon eine der angegebenen Dateien nicht gefunden werden. Der Err. Number-Wert ist 0xc0000bd1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

**Vor Windows Vista:** Sie können keine Protokolldateien aus der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) hinzufügen oder entfernen, wenn der Wert dieser Eigenschaft auf sysmonlogfiles festgelegt ist. Legen Sie den Wert dieser Eigenschaft nach dem Erstellen oder Ändern der Protokolldatei Auflistung auf sysmonlogfiles fest.

Außerdem können Sie die Eigenschaften [**sqldsnname**](systemmonitor-sqldsnname.md) und [**sqllogsetname**](systemmonitor-sqllogsetname.md) nicht ändern, wenn der Wert dieser Eigenschaft nicht auf sysmonsqllog festgelegt werden darf. Legen Sie den Wert dieser Eigenschaft nach dem Ändern der Server-und Datenbanknamen auf sysmonsqllog fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





