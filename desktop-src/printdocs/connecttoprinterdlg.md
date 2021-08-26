---
description: Die ConnectToPrinterDlg-Funktion zeigt ein Dialogfeld an, in dem Benutzer Drucker in einem Netzwerk durchsuchen und eine Verbindung mit ihnen herstellen können.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: ConnectToPrinterDlg-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: f7bbeda17f5cbafa46785577243df9e50b3bf7109631166ffb8894bbb678393e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950430"
---
# <a name="connecttoprinterdlg-function"></a>ConnectToPrinterDlg-Funktion

Die **ConnectToPrinterDlg-Funktion** zeigt ein Dialogfeld an, in dem Benutzer Drucker in einem Netzwerk durchsuchen und eine Verbindung mit ihnen herstellen können. Wenn der Benutzer einen Drucker auswählt, versucht die Funktion, eine Verbindung mit ihm herzustellen. Wenn kein geeigneter Treiber auf dem Server installiert ist, erhält der Benutzer die Möglichkeit, einen Drucker lokal zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Gibt das übergeordnete Fenster des Dialogfelds an.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist und der Benutzer einen Drucker auswählt, ist der Rückgabewert ein Handle für den ausgewählten Drucker.

Wenn die Funktion fehlschlägt oder der Benutzer das Dialogfeld ohne Auswahl eines Druckers abbricht, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die **ConnectToPrinterDlg-Funktion** versucht, eine Verbindung mit dem ausgewählten Drucker herzustellen. Wenn auf dem Server, auf dem sich der Drucker befindet, jedoch kein geeigneter Treiber installiert ist, bietet die Funktion dem Benutzer die Möglichkeit, einen Drucker lokal zu erstellen. Eine aufrufende Anwendung kann bestimmen, ob die Funktion einen Drucker lokal erstellt hat, indem [**GetPrinter**](getprinter.md) mit einer [**PRINTER INFO \_ \_ 2-Struktur**](printer-info-2.md) aufruft und dann das **Attributes-Member** dieser Struktur untersucht wird.

Eine Anwendung sollte [**DeletePrinter aufrufen,**](deleteprinter.md) um einen lokalen Drucker zu löschen. Eine Anwendung sollte [**DeletePrinterConnection aufrufen,**](deleteprinterconnection.md) um eine Verbindung mit einem Drucker zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




