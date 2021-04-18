---
description: Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: GetPrinterDriverPackagePath-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352558"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath-Funktion

Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszserver* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt. Verwenden Sie für den lokalen Computer **null** .

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> <dt>

*pszlanguage* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die [mehrsprachige Benutzeroberflächen](/windows/desktop/Intl/mui-resource-management) Sprache für den installierten Treiber angibt. Dieser Wert kann **null** sein.

</dd> <dt>

*pszpackageid* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die ID des Treiber Pakets angibt.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad zur CAB-Datei für das Treiber Paket angibt. Dieser Wert kann **null** sein. Siehe Hinweise.

</dd> <dt>

*cchDriverPackageCab* \[ in\]
</dt> <dd>

Die Größe des *pszDriverPackageCab* -Puffers in Zeichen. Dieser Wert kann **null** sein.

</dd> <dt>

*pcchrequirements dsize* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die erforderliche Größe des *pszDriverPackageCab* -Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Um einen Wert für *cchDriverPackageCab* zu erhalten, rufen Sie die Funktion mit **null** als Wert von *pszDriverPackageCab* auf. Verwenden Sie den Wert, der in *pcchrequirements dsize* zurückgegeben wurde, als Wert von *cchDriverPackageCab* , und führen Sie die Funktion erneut aus.

*Pszpackageid* wird in der Regel von einem get-Befehl [**getcoreprinterdrivers**](getcoreprinterdrivers.md)abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDriverPackagePathW** (Unicode) und **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

