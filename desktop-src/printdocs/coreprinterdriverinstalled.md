---
description: Die CorePrinterDriverInstalled-Funktion meldet, ob ein Hauptdruckertreiber mit einer angegebenen GUID, einem angegebenen Datum und einer angegebenen Version installiert ist.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: CorePrinterDriverInstalled-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 014b9932046ab6d66b64794bbe042f43a390f9f6a4b6183d36a6338eca434526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719770"
---
# <a name="coreprinterdriverinstalled-function"></a>CorePrinterDriverInstalled-Funktion

Die **CorePrinterDriverInstalled-Funktion** meldet, ob ein Hauptdruckertreiber mit einer angegebenen GUID, einem angegebenen Datum und einer angegebenen Version installiert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszServer* \[ In\]
</dt> <dd>

Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Namen des Druckerservers angibt. Verwenden **Sie NULL** für den lokalen Computer.

</dd> <dt>

*pszEnvironment* \[ In\]
</dt> <dd>

Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die Prozessorarchitektur angibt (z. B. Windows NT x86). Dies kann **NULL sein.**

</dd> <dt>

*CoreDriverGUID* \[ In\]
</dt> <dd>

Die GUID des Hauptdruckertreibers.

</dd> <dt>

*ftDriverDate* \[ In\]
</dt> <dd>

Das Datum des Hauptdruckertreibers.

</dd> <dt>

*dwlDriverVersion* \[ In\]
</dt> <dd>

Die Version des Hauptdruckertreibers.

</dd> <dt>

*pbDriverInstalled* \[ out\]
</dt> <dd>

Ein Zeiger auf **TRUE,** wenn der Treiber oder eine neuere Version installiert ist, **andernfalls FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK, andernfalls enthält **das HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **CorePrinterDriverInstalledW** (Unicode) und **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

