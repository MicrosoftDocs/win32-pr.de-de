---
description: Die \_ PRINTER INFO \_ 7-Struktur gibt Druckerinformationen für Verzeichnisdienste an.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7-Struktur (Winspool.h)
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
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867766"
---
# <a name="printer_info_7-structure"></a>PRINTER \_ INFO \_ 7-Struktur

Die **PRINTER \_ INFO \_ 7-Struktur** gibt Druckerinformationen für Verzeichnisdienste an. Verwenden Sie diese Struktur mit der [**SetPrinter-Funktion,**](setprinter.md) um die Daten eines Druckers im Verzeichnisdienst (Directory Service, DS) zu veröffentlichen oder die veröffentlichten Daten eines Druckers aus dem DS zu aktualisieren oder zu entfernen. Verwenden Sie diese Struktur mit der [**GetPrinter-Funktion,**](getprinter.md) um zu bestimmen, ob ein Drucker im DS veröffentlicht wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Member

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die GUID des einem veröffentlichten Drucker zugeordneten Druckwarteschlangenobjekts des Verzeichnisdiensts enthält. Verwenden Sie die [**GetPrinter-Funktion,**](getprinter.md) um diese GUID abzurufen.

Legen Sie vor dem Aufrufen von [**SetPrinter**](setprinter.md) **pszObjectGUID** auf **NULL** fest.

</dd> <dt>

**dwAction**
</dt> <dd>

Gibt die Aktion an, die die [**SetPrinter-Funktion**](setprinter.md) ausführen soll. Für die [**GetPrinter-Funktion**](getprinter.md) gibt dieser Member an, ob der angegebene Drucker veröffentlicht wird. Dieser Member kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ Ausstehende**</dt> <dt>0x80000000</dt> </dl>       | [**GetPrinter:**](getprinter.md)Gibt an, dass das System versucht, einen Veröffentlichungs- oder Nichtveröffentlichungsvorgang abzuschließen, der durch einen [**SetPrinter-Aufruf**](setprinter.md) gestartet wurde.<br/> [**SetPrinter:**](setprinter.md)Dieser Wert ist ungültig. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBLISH**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter:**](setprinter.md)Veröffentlicht die Druckerdaten im DS.<br/> [**GetPrinter:**](getprinter.md)Gibt an, dass der Drucker veröffentlicht wurde. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ ERNEUTES VERÖFFENTLICHEN**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter:**](setprinter.md)Die DS-Daten für den Drucker werden nicht veröffentlicht und dann erneut veröffentlicht, wobei alle Eigenschaften im veröffentlichten Drucker aktualisiert werden. Die erneute Veröffentlichung ändert auch die GUID des veröffentlichten Druckers.<br/> [**GetPrinter:**](getprinter.md)Gibt diesen Wert nie zurück. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ UNPUBLISH**</dt> <dt>0x00000004</dt> </dl> | [**SetPrinter:**](setprinter.md)Entfernt die veröffentlichten Daten des Druckers aus dem DS.<br/> [**GetPrinter:**](getprinter.md)Gibt an, dass der Drucker nicht veröffentlicht wurde. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ UPDATE**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter:**](setprinter.md)Aktualisiert die veröffentlichten Daten des Druckers im DS.<br/> [**GetPrinter:**](getprinter.md)Gibt diesen Wert nie zurück. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PRINTER \_ INFO \_ 7-Struktur** wird in einem [**SetPrinter-Aufruf**](setprinter.md) verwendet, um Druckerinformationen im Verzeichnisdienst zu veröffentlichen. Die veröffentlichten Daten enthalten alle Werte und Daten für den angegebenen Drucker, die sich unter den SPLDS \_ SPOOLER \_ KEY-, SPLDS \_ DRIVER \_ KEY- oder SPLDS USER KEY-Schlüsseln befinden, die \_ von \_ [**SetPrinterDataEx**](setprinterdataex.md)erstellt wurden.

Für [**SetPrinter**](setprinter.md)sollte *pszObjectGUID* auf **NULL** festgelegt werden. Für [**GetPrinter**](getprinter.md)gibt *pszObjectGUID* die GUID des Druckwarteschlangenobjekts der Verzeichnisdienste zurück, das einem veröffentlichten Drucker zugeordnet ist. Sie können diese GUID mit ADSI-Methoden (Active Directory Services Interface) verwenden, um veröffentlichte Daten für den Drucker abzurufen. Die empfohlene Methode zum Abrufen veröffentlichter Daten ist jedoch der Aufruf der [**GetPrinterDataEx-Funktion.**](getprinterdataex.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 7W** (Unicode) und **\_ PRINTER INFO \_ \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




