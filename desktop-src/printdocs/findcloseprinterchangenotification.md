---
description: Die Funktion FindClosePrinterChangeNotification schließt ein Änderungsbenachrichtigungsobjekt, das durch Aufrufen der FindFirstPrinterChangeNotification-Funktion erstellt wurde.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: FindClosePrinterChangeNotification-Funktion (Winspool.h)
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
ms.openlocfilehash: 17ec31b1f2992b4311e42e149d39b68b3d724a3d943d67df7c4c5fce88122606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112490"
---
# <a name="findcloseprinterchangenotification-function"></a>FindClosePrinterChangeNotification-Funktion

Die **Funktion FindClosePrinterChangeNotification** schließt ein Änderungsbenachrichtigungsobjekt, das durch Aufrufen der [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) erstellt wurde. Der drucker- oder druckserver, der dem Änderungsbenachrichtigungsobjekt zugeordnet ist, wird von diesem Objekt nicht mehr überwacht.

## <a name="syntax"></a>Syntax


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hChange* \[ In\]
</dt> <dd>

Ein Handle für das zu schließende Änderungsbenachrichtigungsobjekt. Dies ist ein Handle, das durch Aufrufen der [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Nachdem Sie die **Funktion FindClosePrinterChangeNotification** aufgerufen haben, können Sie das *hChange-Handle* in nachfolgenden Aufrufen von [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) oder [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)nicht mehr verwenden.

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




