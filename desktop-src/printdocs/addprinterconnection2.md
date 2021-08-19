---
description: Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: AddPrinterConnection2-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f54cdafc2bc5c957f21ed4f9a14355d6a70f7df817e975c1fe701e2b20af35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868968"
---
# <a name="addprinterconnection2-function"></a>AddPrinterConnection2-Funktion

Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWnd* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster, in dem das Dialogfeld angezeigt wird, wenn das Drucksystem einen Druckertreiber vom Druckerserver für diese Verbindung herunterladen muss.

</dd> <dt>

*pszName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante NULL-endende Zeichenfolge, die den Namen des Druckers angibt, mit dem der aktuelle Benutzer eine Verbindung herstellen möchte.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Die Version der -Struktur, auf die *pConnectionInfo* zeigt. Derzeit ist nur Ebene 1 definiert, sodass der Wert von *dwLevel* 1 sein muss.

</dd> <dt>

*pConnectionInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PRINTER \_ CONNECTION INFO \_ \_ 1-Struktur.**](printer-connection-info-1.md) Weitere Informationen zu diesem Parameter finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Rufen [**Sie getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)auf, um erweiterte Fehlerinformationen zu erhalten.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Wenn Windows Vista eine Verbindung mit einem Drucker herstellen, müssen möglicherweise Druckertreiberdateien von dem Server kopiert werden, an den der Drucker angeschlossen ist. Wenn der Benutzer nicht über die Berechtigung zum Kopieren von Dateien an den entsprechenden Speicherort verfügt, schlägt die **Funktion AddPrinterConnection2** fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ ACCESS \_ DENIED zurück.

Wenn die Druckertreiberdateien vom Druckerserver kopiert werden müssen, aber aufgrund der aktivierten Gruppenrichtlinien nicht automatisch kopiert werden können und PRINTER \_ CONNECTION NO UI in \_ \_ *pConnectionInfo->dwFlags* festgelegt ist, werden keine Dialogfelder angezeigt, und der Aufruf schlägt fehl.

Wenn der lokale Druckertreiber zum Rendern von Druckaufträgen für diesen Drucker verwendet werden kann und die Version des lokalen Treibers nicht mit der Version des Druckertreibers auf dem Server übereinstimmen darf, legen Sie PRINTER \_ CONNECTION \_ MISMATCH in *pConnectionInfo->dwFlags* fest, und weisen Sie den Zeiger einer Zeichenfolgenvariablen zu, die den Pfad zum lokalen Druckertreiber enthält, auf *pConnectionInfo->pszDriverName*.

Eine Druckerverbindung, die durch Aufrufen von **AddPrinterConnection2** hergestellt wird, wird aufzählt, wenn [**EnumPrinters**](enumprinters.md) aufgerufen wird und *dwType* auf PRINTER \_ ENUM CONNECTION festgelegt \_ ist.

Die ANSI-Version dieser Funktion, **AddPrinterConnection2A,** wird nicht unterstützt und gibt **ERROR NOT SUPPORTED \_ \_ zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

