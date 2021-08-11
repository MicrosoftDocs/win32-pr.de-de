---
description: Lädt einen Druckertreiber in den Druckerserver-Treiberspeicher hoch, damit er durch Aufrufen von InstallPrinterDriverFromPackage installiert werden kann.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: UploadPrinterDriverPackage-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 15347171299e370bd5e0128976f65e4de1f7034b083b16880ac21659bfac35f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233868"
---
# <a name="uploadprinterdriverpackage-function"></a>UploadPrinterDriverPackage-Funktion

Lädt einen Druckertreiber in den Treiberspeicher des Druckerservers hoch, damit er durch Aufrufen von [**InstallPrinterDriverFromPackage installiert werden kann.**](installprinterdriverfrompackage.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszServer* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Namen des Druckerservers angibt. Verwenden **Sie NULL,** wenn der Server der lokale Computer ist.

</dd> <dt>

*pszInfPath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Quellpfad zur INF-Datei des Treibers angibt.

</dd> <dt>

*pszEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die Prozessorarchitektur des Servers angibt (z. B. Windows NT x86). Dies kann **NULL sein.**

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                     | Bedeutung                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | Die Benutzeroberfläche wird während des Uploads nicht angezeigt.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | Die Dateien werden auch dann hochgeladen, wenn sich das Paket bereits im Treiberspeicher des Servers befindet.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | Der Treiberspeicher des Servers wird vor dem Hochladen überprüft, um zu überprüfen, ob das Paket bereits vorhanden ist. Diese Einstellung wird ignoriert, wenn UPDP_UPLOAD_ALWAYS festgelegt ist.<br/> |



 

</dd> <dt>

*hwnd* \[ In\]
</dt> <dd>

Ein Handle für die kopierende Benutzeroberfläche.

</dd> <dt>

*pszDestInfPath* \[ out\]
</dt> <dd>

Ein Zeiger auf den Zielpfad im Treiberspeicher, in den die INF-Datei des Treibers kopiert wurde.

</dd> <dt>

*pcchDestInfPath* \[ in, out\]
</dt> <dd>

Gibt bei der Eingabe die Größe des *pszDestInfPath-Puffers* in Zeichen an. Empfängt bei der Ausgabe die Größe der Pfadzeichenfolge in Zeichen, einschließlich des beendenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, wird der Rückgabewert S_OK, andernfalls enthält **das HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu kommen, dass die Anwendung nicht reagiert.

 

Der Treiberspeicher ist in der Regel entweder %windir% \\ inf oder %windir% \\ System32 \\ DriverStore \\ FileRepository.

Es kann immer nur ein Paket gleichzeitig hochgeladen werden. Wenn ein Paket von anderen abhängig ist, müssen sie separat hochgeladen werden.

Nur signierte Treiberpakete können hochgeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **UploadPrinterDriverPackageW** (Unicode) und **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

