---
description: Ruft ein Handle für den angegebenen Drucker, Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: OpenPrinter2-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865868"
---
# <a name="openprinter2-function"></a>OpenPrinter2-Funktion

Ruft ein Handle für den angegebenen Drucker, Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden.

## <a name="syntax"></a>Syntax


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprintername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante mit NULL endender Zeichenfolge, die den Namen des Druckers oder Druck Servers, das Drucker Objekt, den xcvmonitor oder den xcvport angibt.

Verwenden Sie für ein Drucker Objekt: PrinterName, Job xxxx. Verwenden Sie für einen xcvmonitor Folgendes: Servername, xcvmonitor Monitorname. Verwenden Sie für einen xcvport: Servername, xcvport PORTNAME.

**Windows Vista:** Wenn der Wert **null** ist, wird der lokale Drucker Server angegeben.

</dd> <dt>

*phprinter* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den geöffneten Drucker oder das Druckserver Objekt empfängt.

</dd> <dt>

*pdefault* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur. Dieser Wert kann **null** sein.

</dd> <dt>

*poptions* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Drucker \_ options**](printer-options.md) Struktur. Dieser Wert kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Für erweiterte Fehlerinformationen aufrufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Bemerkungen

Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die ANSI-Version dieser Funktion ist nicht implementiert und gibt einen Fehler zurück, der \_ nicht \_ unterstützt wird.

Mit dem *pdefault* -Parameter können Sie die Werte für Datentyp und Geräte Modus angeben, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion übermittelt werden. Sie können diese Werte jedoch überschreiben, indem Sie die Funktion [**setjob**](setjob.md) verwenden, nachdem ein Dokument gestartet wurde.

Sie können die **OpenPrinter2** -Funktion aufrufen, um ein Handle für einen Druckserver zu öffnen oder um die Client Zugriffsrechte für einen Druckserver zu ermitteln. Geben Sie hierzu den Namen des Drucker Servers im *pprintername* -Parameter an, legen Sie die **pdatatype** -und **pdevmode** -Member der [**\_ Standard**](printer-defaults.md) Struktur der Drucker Standards auf **null** fest, und legen Sie für das **desiredAccess** -Element einen Server Zugriffs Maskenwert fest, wie z \_ . b. Zugriff auf den Server \_ . Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.

Verwenden Sie das **desiredAccess** -Mitglied [**der \_ Drucker Standard**](printer-defaults.md) Struktur, um die erforderlichen Zugriffsrechte anzugeben. Die Zugriffsrechte können eines der folgenden sein:



| Gewünschter Zugriffs Wert                        | Bedeutung                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Zugriffs \_ Verwaltung                 | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.                                                                                                 |
| Drucker \_ Zugriffs \_ Verwendung                        | Zum Ausführen grundlegender Druckvorgänge.                                                                                                                                                        |
| Drucker \_ \_ Zugriff                        | Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge außer synchronisieren. Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).                                         |
| Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung            | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten. Dieser Wert ist ab Windows 8.1 verfügbar. |
| generische Sicherheitswerte, z. b. \_ DAC schreiben | , Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen. Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Wenn ein Benutzer nicht über die Berechtigung zum Öffnen eines angegebenen Druckers oder Druck Servers mit dem gewünschten Zugriff verfügt, schlägt der **OpenPrinter2** -Befehl fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Wert für den Fehler \_ Zugriff \_ verweigert zurück.

Wenn " *pprintername* " ein lokaler Drucker ist, ignoriert **OpenPrinter2** alle Werte der **dwFlags** , auf die die Struktur der Druckeroptionen mithilfe von *poptions* zeigt, mit Ausnahme der Option "Client Änderung für Drucker [**\_ Optionen**](printer-options.md) " \_ \_ \_ . Wenn Letzteres erfolgreich ist, gibt **OpenPrinter2** die Fehlermeldung " \_ Zugriff \_ verweigert" zurück. Dementsprechend bietet **OpenPrinter2** beim Öffnen eines lokalen Druckers keinen Vorteil gegenüber [**OpenPrinter**](openprinter.md).

**Windows Vista:** Die von **OpenPrinter2** zurückgegebenen Druckerdaten werden aus einem lokalen Cache abgerufen, es sei denn, die **\_ Druckeroption \_ kein \_ Cache** -Flag wird im **dwFlags** -Feld der [**Drucker \_ options**](printer-options.md) Struktur festgelegt, auf die durch *poptions* verwiesen wird.

## <a name="examples"></a>Beispiele

In diesem Beispiel schlägt **OpenPrinter2** fehl, wenn der Drucker \_ Zugriffs \_ Verwaltung \_ Limited an die [**Drucker \_ Standard**](printer-defaults.md) Struktur übermittelt wird und der Benutzer nicht über die entsprechende Berechtigung verfügt.


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



Ein Beispielprogramm, das zeigt, wie diese Funktion verwendet wird, finden Sie unter Gewusst [wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **OpenPrinter2W** (Unicode) und **OpenPrinter2A** (ANSI)<br/>                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Drucker \_ Standardwerte**](printer-defaults.md)
</dt> <dt>

[**Drucker \_ Optionen**](printer-options.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

