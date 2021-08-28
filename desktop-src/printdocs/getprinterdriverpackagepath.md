---
description: Ruft den Pfad zum angegebenen Druckertreiberpaket auf einem Druckerserver ab.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: GetPrinterDriverPackagePath-Funktion (Winspool.h)
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
ms.openlocfilehash: 5058d57a0275019c5e603673d260c9969cc0b5d5641dea15e09ffe242addff10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600800"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath-Funktion

Ruft den Pfad zum angegebenen Druckertreiberpaket auf einem Druckerserver ab.

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

*pszServer* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Namen des Druckerservers angibt. Verwenden **Sie NULL** für den lokalen Computer.

</dd> <dt>

*pszEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die Prozessorarchitektur angibt (z. B. Windows NT x86). Dies kann **NULL sein.**

</dd> <dt>

*pszLanguage* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die mehrsprachige Benutzeroberfläche [sprache](/windows/desktop/Intl/mui-resource-management) für den installierten Treiber angibt. Dies kann **NULL sein.**

</dd> <dt>

*pszPackageID* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die ID des Treiberpakets angibt.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad zur Schränkdatei für das Treiberpaket angibt. Dies kann **NULL sein.** Siehe Hinweise.

</dd> <dt>

*cchDriverPackageCab* \[ In\]
</dt> <dd>

Die Größe des Puffers *pszDriverPackageCab* in Zeichen. Dies kann **NULL sein.**

</dd> <dt>

*pcchRequiredSize* \[ out\]
</dt> <dd>

Ein Zeiger auf die erforderliche Größe des *pszDriverPackageCab-Puffers.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK, andernfalls enthält **das HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Um einen Wert für *cchDriverPackageCab* zu erhalten, rufen Sie die Funktion mit **NULL** als Wert von *pszDriverPackageCab auf.* Verwenden Sie den in *pcchRequiredSize* zurückgegebenen Wert als Wert von *cchDriverPackageCab,* und rufen Sie die Funktion erneut auf.

Die *pszPackageID* wird in der Regel durch einen Aufruf von [**GetCorePrinterDrivers erhalten.**](getcoreprinterdrivers.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDriverPackagePathW** (Unicode) und **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

