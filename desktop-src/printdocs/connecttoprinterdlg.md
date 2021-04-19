---
description: Die connecttoprinterdlg-Funktion zeigt ein Dialogfeld an, mit dem Benutzer in einem Netzwerk nach Druckern suchen und eine Verbindung mit Ihnen herstellen können.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Connecttoprinterdlg-Funktion (winspool. h)
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
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366178"
---
# <a name="connecttoprinterdlg-function"></a>Connecttoprinterdlg-Funktion

Die **connecttoprinterdlg** -Funktion zeigt ein Dialogfeld an, mit dem Benutzer in einem Netzwerk nach Druckern suchen und eine Verbindung mit Ihnen herstellen können. Wenn der Benutzer einen Drucker auswählt, versucht die Funktion, eine Verbindung damit herzustellen. Wenn ein geeigneter Treiber nicht auf dem Server installiert ist, erhält der Benutzer die Möglichkeit, einen Drucker lokal zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Gibt das übergeordnete Fenster des Dialog Felds an.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird und der Benutzer einen Drucker auswählt, ist der Rückgabewert ein Handle für den ausgewählten Drucker.

Wenn die Funktion fehlschlägt oder der Benutzer das Dialogfeld abbricht, ohne einen Drucker auszuwählen, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die **connecttoprinterdlg** -Funktion versucht, eine Verbindung mit dem ausgewählten Drucker herzustellen. Wenn auf dem Server, auf dem der Drucker residiert, jedoch kein geeigneter Treiber installiert ist, bietet die Funktion dem Benutzer die Möglichkeit, einen Drucker lokal zu erstellen. Eine aufrufenden Anwendung kann ermitteln, ob die Funktion einen Drucker lokal erstellt hat, indem Sie [**GetPrinter**](getprinter.md) mit einer [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur aufgerufen hat, und dann den **Attributmember** der Struktur untersucht.

Eine Anwendung sollte [**deleteprinter**](deleteprinter.md) aufrufen, um einen lokalen Drucker zu löschen. Eine Anwendung sollte [**deleteprinterconnection**](deleteprinterconnection.md) aufrufen, um eine Verbindung mit einem Drucker zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**"AddPrinterConnection"**](addprinterconnection.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Deleteprinter**](deleteprinter.md)
</dt> <dt>

[**Deleteprinterconnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




