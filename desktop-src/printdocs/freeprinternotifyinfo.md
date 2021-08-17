---
description: Die FreePrinterNotifyInfo-Funktion gibt einen vom System zugeordneten Puffer frei, der von der FindNextPrinterChangeNotification-Funktion erstellt wurde.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: FreePrinterNotifyInfo-Funktion (Winspool.h)
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
ms.openlocfilehash: 37340bc7d5ba576735c7bf4cc1ef8ac40b07377e829353d35452ed0fa5307891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091950"
---
# <a name="freeprinternotifyinfo-function"></a>FreePrinterNotifyInfo-Funktion

Die **FreePrinterNotifyInfo-Funktion** gibt einen vom System zugeordneten Puffer frei, der von der [**FindNextPrinterChangeNotification-Funktion**](findnextprinterchangenotification.md) erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPrinterNotifyInfo* \[ In\]
</dt> <dd>

Zeiger auf einen [**PRINTER \_ NOTIFY \_ INFO-Puffer,**](printer-notify-info.md) der von einem Aufruf der [**FindNextPrinterChangeNotification-Funktion**](findnextprinterchangenotification.md) zurückgegeben wird. **FreePrinterNotifyInfo** hebt die Zuordnung dieses Puffers auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_ \_ DRUCKERBENACHRICHTIGUNGSINFORMATIONEN**](printer-notify-info.md)
</dt> </dl>

 

 




