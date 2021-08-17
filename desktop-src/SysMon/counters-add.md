---
title: Counters.Add-Methode
description: Fügt der Auflistung eine CounterItem-Instanz hinzu.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Hinzufügen der SysMon-Methode
- Hinzufügen der SysMon-Methode, Counters-Klasse
- Counters-Klasse SysMon , Add-Methode
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36d2b9bdc2edc9565b1eac5ebae335e5fbad80752f572c48c0f1b05c9668de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883398"
---
# <a name="countersadd-method"></a>Counters.Add-Methode

Fügt der [**Auflistung eine CounterItem-Instanz**](counteritem.md) hinzu.

## <a name="syntax"></a>Syntax


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pathname* \[ In\]
</dt> <dd>

Pfad zum Zähler. Der Pfad kann einen Computernamen enthalten und muss einen Leistungsobjektnamen, einen Objektinstanznamen, wenn das angegebene Leistungsobjekt mehrere Instanzen unterstützt, und einen Indikatornamen enthalten. Bei dieser Pfadspezifikation wird die Kleinschreibung nicht beachtet.

Weitere Informationen zum Angeben eines Indikatorpfads finden Sie unter [Angeben eines Indikatorpfads.](/windows/desktop/PerfCtrs/specifying-a-counter-path)

</dd> </dl>

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
<td><strong>System.Runtime.InteropServices.COMException</strong></td>
<td>Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:
<ul>
<li>Das angegebene Leistungsobjekt wurde auf dem Computer nicht gefunden. Der Err.Number-Wert ist 0xC0000BB8.</li>
<li>Der angegebene Zähler wurde nicht gefunden. Der Err.Number-Wert ist 0xC0000BB9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Wenn Sie einen Platzhalterzähler im *Pathname-Parameter* angeben, erstellt die **Add-Methode** ein [**CounterItem-Objekt**](counteritem.md) für jeden erweiterten Pfad. Die **Add-Methode** gibt dann einen Zeiger auf das erste hinzugefügte **CounterItem zurück.**

Wenn der Platzhalter zu einem doppelten Leistungsindikator führen würde, wird der Fehler nicht gemeldet, und es wird kein Duplikat erstellt. Wenn eine Fehlerbedingung auftritt, bevor alle Leistungsindikatoren erstellt werden, wird der Fehler gemeldet, und die verbleibenden Leistungsindikatoren werden nicht erstellt.

Es gibt keine Beschränkung für die Anzahl von Leistungsindikatoren, die Sie hinzufügen können. SYSMON zeigt jedoch nur die ersten 1.024 Leistungsindikatoren in der Auflistung an. Es gibt keine Beschränkung für die Anzahl der Leistungsindikatoren, die SYSMON in einem Bericht anzeigen wird.

Implementieren Sie das [OnCounterAdded-Ereignis,](systemmonitor-oncounteradded.md) um Benachrichtigungen zu erhalten, wenn ein Zähler hinzugefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

