---
description: Die Funktion "freprinternotifyinfo" gibt einen vom System zugewiesenen Puffer frei, der von der findnextprinterchangenotifi-Funktion erstellt wurde.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Freprinternotifyinfo-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347351"
---
# <a name="freeprinternotifyinfo-function"></a>Freprinternotifyinfo-Funktion

Die Funktion " **freprinternotifyinfo** " gibt einen vom System zugewiesenen Puffer frei, der von der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprinternotifyinfo* \[ in\]
</dt> <dd>

Zeiger auf einen [**Drucker \_ Benachrichtigungs \_**](printer-notify-info.md) Puffer, der von einem aufrufsbefehl der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion zurückgegeben wird. " **Freiprinternotifyinfo** " hebt die Zuordnung dieses Puffers auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

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

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Informationen**](printer-notify-info.md)
</dt> </dl>

 

 




