---
description: Lädt einen Druckertreiber in den Drucker Server-Treiber Speicher hoch, damit er durch Aufrufen von installprinterdriverfrompackage installiert werden kann.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Uploadprinterdriverpackage-Funktion (winspool. h)
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
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217837"
---
# <a name="uploadprinterdriverpackage-function"></a>Uploadprinterdriverpackage-Funktion

Lädt einen Druckertreiber in den Treiber Speicher des Druck Servers hoch, sodass er durch Aufrufen von [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md)installiert werden kann.

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

*pszserver* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt. Verwenden Sie **null** , wenn der Server der lokale Computer ist.

</dd> <dt>

*pszinfpath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Quellpfad zur INF-Datei des Treibers angibt.

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur des Servers angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dabei kann es sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                                     | Bedeutung                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | Die Benutzeroberfläche wird während des Uploads nicht angezeigt.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | Die Dateien werden auch dann hochgeladen, wenn das Paket bereits im Treiber Speicher des Servers vorhanden ist.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | Der Treiber Speicher des Servers wird vor dem Hochladen geprüft, um festzustellen, ob das Paket bereits vorhanden ist. Diese Einstellung wird ignoriert, wenn UPDP_UPLOAD_ALWAYS festgelegt ist.<br/> |



 

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Handle für die kopierende Benutzeroberfläche.

</dd> <dt>

*pszdestinfpath* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Zielpfad im Treiber Speicher, in den die INF-Datei des Treibers kopiert wurde.

</dd> <dt>

*pcchdestinfpath* \[ in, out\]
</dt> <dd>

Gibt bei der Eingabe die Größe des *pszdestinfpath* -Puffers in Zeichen an. Bei der Ausgabe empfängt die Größe der Pfad Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, wird der Rückgabewert S_OK, andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der Treiber Speicher ist in der Regel entweder% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.

Es kann immer nur jeweils ein Paket hochgeladen werden. Wenn ein Paket von anderen abhängig ist, müssen diese separat hochgeladen werden.

Nur signierte Treiber Pakete können hochgeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **UploadPrinterDriverPackageW** (Unicode) und **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

