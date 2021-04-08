---
title: System Monitor-browscounters-Methode
description: Zeigt das Dialogfeld Leistungsindikatoren hinzufügen an.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Browscounters-Methode (Sysmon)
- Browscounters-Methode (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, browscounters-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040064"
---
# <a name="systemmonitorbrowsecounters-method"></a>System Monitor:: browscounters-Methode

Zeigt das Dialogfeld Leistungsindikatoren **Hinzufügen** an.

## <a name="syntax"></a>Syntax


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In diesem Dialogfeld können Benutzer lokale oder Remote-Leistungsindikatoren aus einer Liste von Leistungs Objekten auswählen. Die ausgewählten Leistungsindikatoren werden der [**Zähler**](counters.md) Sammlung hinzugefügt und im Diagramm oder Bericht angezeigt.

Um eine Benachrichtigung zu erhalten, wenn ein Indikator hinzugefügt wird, implementieren Sie das [**oncounteradded**](systemmonitor-oncounteradded.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Zähler. Add**](counters-add.md)
</dt> </dl>

 

 





