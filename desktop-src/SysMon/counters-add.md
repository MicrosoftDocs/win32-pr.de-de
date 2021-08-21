---
title: Counters.Add-Methode
description: Fügt der Auflistung eine CounterItem-Instanz hinzu.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Hinzufügen der SysMon-Methode
- Hinzufügen der SysMon-Methode , Counters-Klasse
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
ms.openlocfilehash: a8d8169980de00338c7fdd0b804013f986a5a7ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466007"
---
# <a name="countersadd-method"></a>Counters.Add-Methode

Fügt der Auflistung eine [**CounterItem-Instanz**](counteritem.md) hinzu.

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

Pfad zum Leistungsindikator. Der Pfad kann einen Computernamen und einen Leistungsobjektnamen, einen Objektinstanznamen, wenn das angegebene Leistungsobjekt mehrere Instanzen unterstützt, und einen Indikatornamen enthalten. Bei dieser Pfadspezifikation wird die Groß-/Kleinschreibung nicht beachtet.

Ausführliche Informationen zum Angeben eines Indikatorpfads finden Sie unter [Angeben eines Indikatorpfads.](/windows/desktop/PerfCtrs/specifying-a-counter-path)

</dd> </dl>

## <a name="exceptions"></a>Ausnahmen




| Ausnahmetyp | Bedingung | 
|----------------|-----------|
| <strong>System.Runtime.InteropServices.COMException</strong> | Sie können diese Ausnahme aus einem der folgenden Gründe erhalten:<ul><li>Das angegebene Leistungsobjekt wurde auf dem Computer nicht gefunden. Der Err.Number-Wert ist 0xC0000BB8.</li><li>Der angegebene Indikator konnte nicht gefunden werden. Der Err.Number-Wert ist 0xC0000BB9.</li></ul> | 




 

## <a name="remarks"></a>Hinweise

Wenn Sie im *Pathname-Parameter* einen Platzhalterzähler angeben, erstellt die **Add-Methode** ein [**CounterItem-Objekt**](counteritem.md) für jeden erweiterten Pfad. Die **Add-Methode** gibt dann einen Zeiger auf das erste **hinzugefügte CounterItem** zurück.

Wenn der Platzhalter zu einem doppelten Indikator führen würde, wird der Fehler nicht gemeldet, und es wird kein Duplikat erstellt. Wenn eine Fehlerbedingung auftritt, bevor alle Leistungsindikatoren erstellt werden, wird der Fehler gemeldet, und die verbleibenden Leistungsindikatoren werden nicht erstellt.

Es gibt keine Beschränkung für die Anzahl von Indikatoren, die Sie hinzufügen können. SYSMON graphiert jedoch nur die ersten 1.024 Leistungsindikatoren in der Sammlung. Es gibt keine Beschränkung für die Anzahl der Leistungsindikatoren, die SYSMON in einem Bericht anzeigt.

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

 

