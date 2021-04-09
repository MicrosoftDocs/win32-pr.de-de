---
description: Die Funktion findcloseprinterchangenotifischließt ein Änderungs Benachrichtigungs Objekt, das durch Aufrufen der findfirstprinterchangenotifizierungsfunktion erstellt wurde.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Findcloseprinterchangenotifi-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042214"
---
# <a name="findcloseprinterchangenotification-function"></a>Findcloseprinterchangenotifi-Funktion

Die Funktion **findcloseprinterchangenotifischließt** ein Änderungs Benachrichtigungs Objekt, das durch Aufrufen der [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) erstellt wurde. Der Drucker oder Druckserver, der dem Änderungs Benachrichtigungs Objekt zugeordnet ist, wird nicht mehr von diesem Objekt überwacht.

## <a name="syntax"></a>Syntax


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hchange* \[ in\]
</dt> <dd>

Ein Handle für das Änderungs Benachrichtigungs Objekt, das geschlossen werden soll. Dies ist ein Handle, das durch Aufrufen der [**findfirstprinterchangenotifi-**](findfirstprinterchangenotification.md) Funktion erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Nachdem Sie die **findcloseprinterchangenotifi-** Funktion aufgerufen haben, können Sie das *hchange* -Handle nicht in nachfolgenden Aufrufen von [**findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md) oder [**findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md)
</dt> <dt>

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




