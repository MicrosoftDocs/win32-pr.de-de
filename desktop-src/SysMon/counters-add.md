---
title: Counters. Add-Methode
description: Fügt der Auflistung eine-Instanz hinzu.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Methode hinzufügen (Sysmon)
- Add-Methode (Sysmon), counters-Klasse
- Zähler Klasse sysmon, Methode hinzufügen
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
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475828"
---
# <a name="countersadd-method"></a>Counters. Add-Methode

Fügt der [**Auflistung eine-**](counteritem.md) Instanz hinzu.

## <a name="syntax"></a>Syntax


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Der Pfad des Zählers. Der Pfad kann einen Computernamen enthalten und muss einen Leistungs Objektnamen, einen objektinstanznamen, wenn das angegebene Leistungs Objekt mehrere Instanzen unterstützt, und einen Leistungs Namen enthalten. Bei dieser Pfadangabe wird die Groß-/Kleinschreibung nicht beachtet.

Ausführliche Informationen zum Angeben eines Zählers finden Sie unter [Angeben eines Counter-Pfads](/windows/desktop/PerfCtrs/specifying-a-counter-path).

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
<td><strong>System. Runtime. InteropServices. COMException</strong></td>
<td>Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:
<ul>
<li>Das angegebene Leistungs Objekt wurde auf dem Computer nicht gefunden. Der Err. Number-Wert ist 0xc0000bb8.</li>
<li>Der angegebene Counter konnte nicht gefunden werden. Der Err. Number-Wert ist 0xc0000bb9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Platzhalter Indikator im *Pfadnamen* -Parameter angeben, erstellt die **Add** -Methode ein Objekt vom Typ " [**count**](counteritem.md) " für jeden erweiterten Pfad. Die **Add** -Methode gibt dann einen Zeiger auf das erste hinzugefügte **ratteritem** zurück.

Wenn der Platzhalter zu einem doppelten Zählers führt, wird der Fehler nicht gemeldet, und es wird kein Duplikat erstellt. Wenn vor dem Erstellen aller Indikatoren eine Fehlerbedingung auftritt, wird der Fehler gemeldet, und die verbleibenden Leistungsindikatoren werden nicht erstellt.

Es gibt keine Beschränkung für die Anzahl der Leistungsindikatoren, die Sie hinzufügen können. sysmon zeigt jedoch nur die ersten 1.024-Leistungsindikatoren in der Sammlung an. Es gibt keine Beschränkung für die Anzahl von Leistungsindikatoren, die in einem Bericht von sysmon angezeigt werden.

Um eine Benachrichtigung zu erhalten, wenn ein Indikator hinzugefügt wird, implementieren Sie das [oncounteradded](systemmonitor-oncounteradded.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**Systemmonitor. browsekunden**](systemmonitor-browsecounters.md)
</dt> </dl>

 

