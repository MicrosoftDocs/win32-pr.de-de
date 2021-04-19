---
description: Die Drucker \_ Info \_ 7-Struktur gibt Verzeichnisdienst-Drucker Informationen an.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357026"
---
# <a name="printer_info_7-structure"></a>Drucker \_ Info \_ 7-Struktur

Die **Drucker \_ Info \_ 7** -Struktur gibt Verzeichnisdienst-Drucker Informationen an. Verwenden Sie diese Struktur mit der [**SetPrinter**](setprinter.md) -Funktion, um die Daten eines Druckers im Verzeichnisdienst (DS) zu veröffentlichen oder um die veröffentlichten Daten eines Druckers aus den DS zu aktualisieren oder zu entfernen. Verwenden Sie diese Struktur mit der [**GetPrinter**](getprinter.md) -Funktion, um zu bestimmen, ob ein Drucker in DS veröffentlicht wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Member

<dl> <dt>

**pszobjectguid**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die GUID des Verzeichnisdienst-Druck Warteschlangen Objekts enthält, das einem veröffentlichten Drucker zugeordnet ist. Verwenden Sie die [**GetPrinter**](getprinter.md) -Funktion, um diese GUID abzurufen.

Legen Sie **pszobjectguid** vor dem Aufrufen von [**SetPrinter**](setprinter.md)auf **null** fest.

</dd> <dt>

**dwAction**
</dt> <dd>

Gibt die Aktion an, die von der [**SetPrinter**](setprinter.md) -Funktion ausgeführt werden soll. Bei der [**GetPrinter**](getprinter.md) -Funktion gibt dieser Member an, ob der angegebene Drucker veröffentlicht wird. Dieser Member kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**Dsprint \_ Ausstehende**</dt> <dt>0x80000000</dt> </dl>       | [**GetPrinter**](getprinter.md): gibt an, dass das System versucht, einen Vorgang zum Veröffentlichen oder Aufheben der Veröffentlichung auszuführen, der von einem [**SetPrinter**](setprinter.md) -Befehl gestartet wurde.<br/> [**SetPrinter**](setprinter.md): dieser Wert ist ungültig. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**Dsprint \_**</dt> <dt>0x00000001</dt> veröffentlichen </dl>       | [**SetPrinter**](setprinter.md): veröffentlicht die Druckerdaten in DS.<br/> [**GetPrinter**](getprinter.md): gibt an, dass der Drucker veröffentlicht wird. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**Dsprint \_**</dt> <dt>0x00000008</dt> erneut veröffentlichen </dl> | [**SetPrinter**](setprinter.md): die DS-Daten für den Drucker werden nicht veröffentlicht und dann erneut veröffentlicht, sodass alle Eigenschaften im veröffentlichten Drucker aktualisiert werden. Bei der erneuten Veröffentlichung wird auch die GUID des veröffentlichten Druckers geändert.<br/> [**GetPrinter**](getprinter.md): gibt diesen Wert nie zurück. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**Dsprint \_ Veröffentlichung**</dt> von <dt>0x00000004</dt> aufheben </dl> | [**SetPrinter**](setprinter.md): entfernt die veröffentlichten Daten des Druckers aus dem DS.<br/> [**GetPrinter**](getprinter.md): gibt an, dass der Drucker nicht veröffentlicht wurde. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**Dsprint \_**</dt> <dt>0x00000002</dt> aktualisieren </dl>          | [**SetPrinter**](setprinter.md): aktualisiert die veröffentlichten Daten des Druckers in DS.<br/> [**GetPrinter**](getprinter.md): gibt diesen Wert nie zurück. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Drucker \_ Info \_ 7** -Struktur wird in einem [**SetPrinter**](setprinter.md) -Befehl verwendet, um Drucker Informationen im Verzeichnisdienst zu veröffentlichen. Die veröffentlichten Daten umfassen alle Werte und Daten für den angegebenen Drucker, der sich unter dem \_ spoolerschlüssel (splds Spooler \_ Key, splds \_ Driver Key) befindet \_ , oder die \_ \_ von [**setprinterdataex**](setprinterdataex.md)erstellten Benutzerschlüssel Schlüssel von splds.

Für [**SetPrinter**](setprinter.md)sollte *pszobjectguid* auf **null** festgelegt werden. Bei [**GetPrinter**](getprinter.md)gibt *pszobjectguid* die GUID des druckwarteschlangenobjekts der Verzeichnisdienste zurück, das einem veröffentlichten Drucker zugeordnet ist. Sie können diese GUID mit ADSI-Methoden (Active Directory Services Interface) verwenden, um veröffentlichte Daten für den Drucker abzurufen. Die empfohlene Methode zum Abrufen veröffentlichter Daten ist jedoch das Aufrufen der [**getprinterdataex**](getprinterdataex.md) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Informationen \_ 7W** (Unicode) und **\_ Drucker \_ Info \_ 7a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




