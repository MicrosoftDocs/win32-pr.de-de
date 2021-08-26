---
description: Die ConfigurePort-Funktion zeigt das Dialogfeld port-configuration für einen Port auf dem angegebenen Server an.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: ConfigurePort-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dbc31de341c137e8baf729a468e8576684ccef8b0a860be898c9cb5a6af34217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950440"
---
# <a name="configureport-function"></a>ConfigurePort-Funktion

Die **ConfigurePort-Funktion** zeigt das Dialogfeld port-configuration für einen Port auf dem angegebenen Server an.

## <a name="syntax"></a>Syntax


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der angegebene Port vorhanden ist. Wenn dieser Parameter **NULL** ist, ist der Port lokal.

</dd> <dt>

*hWnd* \[ In\]
</dt> <dd>

Handle für das übergeordnete Fenster des Dialogfelds "Portkonfiguration".

</dd> <dt>

*pPortName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu konfigurierenden Ports angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Vor dem Aufrufen der **ConfigurePort-Funktion** sollte eine Anwendung die [**EnumPorts-Funktion**](enumports.md) aufrufen, um gültige Portnamen zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **ConfigurePortW** (Unicode) und **ConfigurePortA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




