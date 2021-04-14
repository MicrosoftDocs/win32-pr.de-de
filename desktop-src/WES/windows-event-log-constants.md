---
title: Windows-Ereignisprotokoll Konstanten (winevt. h)
description: 'Das Windows-Ereignisprotokoll definiert die folgenden Konstanten:'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391889"
---
# <a name="windows-event-log-constants"></a>Windows-Ereignisprotokoll Konstanten

Das Windows-Ereignisprotokoll definiert die folgenden Konstanten:

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT \_ Variant \_ - \_ typmaske**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Eine Bitmaske, die Sie zum Maskieren des arraybits des Variant-Typs verwenden, damit Sie den Datentyp des Variant-Werts ermitteln können, der in der [**EVT- \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) -Struktur enthalten ist.


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**Array von EVT- \_ Variant- \_ Typ \_**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



Der **Typmember** der [**EVT- \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) -Struktur ist dieses Bit festgelegt, wenn die Variante einen Zeiger auf ein Array von Werten enthält, nicht auf den Wert selbst.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT- \_ Lese \_ Zugriff**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Lese Zugriffs Steuerungs Berechtigung, die das Lesen von Informationen aus einem Ereignisprotokoll zulässt.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT- \_ Schreib \_ Zugriff**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Schreibzugriffs Steuerungs Berechtigung, mit der Informationen in ein Ereignisprotokoll geschrieben werden können.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**\_ \_ Zugriff löschen**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Löschen Sie die Zugriffs Steuerungs Berechtigung, mit der alle Informationen aus einem Ereignisprotokoll gelöscht werden können.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**sämtlichen \_ \_ Zugriff**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Alle (lesen, schreiben, löschen und löschen) Zugriffs Steuerungs Berechtigung.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Winevt. h</dt> </dl> |



 

 





