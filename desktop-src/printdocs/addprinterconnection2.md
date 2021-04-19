---
description: Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: AddPrinterConnection2-Funktion (winspool. h)
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
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347987"
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

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster, in dem das Dialogfeld angezeigt wird, wenn das Drucksystem einen Druckertreiber vom Druckserver für diese Verbindung herunterladen muss.

</dd> <dt>

*pszName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante mit NULL endenden Zeichenfolge, die den Namen des Druckers angibt, mit dem der aktuelle Benutzer eine Verbindung herstellen möchte.

</dd> <dt>

*dwlevel* 
</dt> <dd>

Die Version der Struktur, auf die von *pconnectioninfo* verwiesen wird. Derzeit wird nur Ebene 1 definiert, sodass der Wert von *dwlevel* 1 lauten muss.

</dd> <dt>

*pconnectioninfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die Struktur der [**Drucker \_ Verbindungs \_ Informationen \_ 1**](printer-connection-info-1.md) . Weitere Informationen zu diesem Parameter finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Für erweiterte Fehlerinformationen aufrufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Wenn Windows Vista eine Verbindung zu einem Drucker herstellt, müssen möglicherweise Druckertreiber Dateien von dem Server, an den der Drucker angefügt ist, kopiert werden. Wenn der Benutzer nicht über die Berechtigung zum Kopieren von Dateien an den entsprechenden Speicherort verfügt, schlägt die **AddPrinterConnection2** -Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler " \_ Zugriff verweigert" zurück \_ .

Wenn die Druckertreiber Dateien vom Druckserver kopiert werden müssen, aber nicht automatisch kopiert werden können, da die Gruppenrichtlinien wirksam sind und die Drucker \_ Verbindung \_ keine \_ Benutzeroberfläche in *pconnectioninfo->dwFlags* festgelegt ist, werden keine Dialogfelder angezeigt, und der Aufruf schlägt fehl.

Wenn der lokale Druckertreiber zum renderingdruck von Druckaufträgen für diesen Drucker verwendet werden kann und die Version des lokalen Treibers nicht mit der Version des Druckertreibers auf dem Server identisch ist, legen Sie \_ den Drucker Verbindungs Konflikt \_ in *pconnectioninfo->dwFlags* fest, und weisen Sie den Zeiger einer Zeichen folgen Variablen zu, die den Pfad des lokalen Druckertreibers zu *pconnectioninfo->pszdrivername* enthält.

Eine Druckerverbindung, die durch den Aufruf von **AddPrinterConnection2** hergestellt wird, wird aufgezählt, wenn [**enumprinter**](enumprinters.md) aufgerufen wird, wobei *dwType* auf druckerenum-Verbindung festgelegt ist \_ \_ .

Die ANSI-Version dieser Funktion, **AddPrinterConnection2A**, wird nicht unterstützt und gibt einen Fehler zurück, der **\_ nicht \_ unterstützt** wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Connecttoprinterdlg**](connecttoprinterdlg.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**Deleteprinterconnection**](deleteprinterconnection.md)
</dt> </dl>

 

