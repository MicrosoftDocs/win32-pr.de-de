---
description: Die EnumForms-Funktion listet die vom angegebenen Drucker unterstützten Formulare auf.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: EnumForms-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e5ce18e81e4d775fdc801517867491740a7dd5035fc730226cb084e5af7d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732698"
---
# <a name="enumforms-function"></a>EnumForms-Funktion

Die **EnumForms-Funktion** listet die vom angegebenen Drucker unterstützten Formulare auf.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für den Drucker, für den die Formulare aufzählt werden sollen. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Gibt die Version der -Struktur an, auf die *pForm* verweist. Dieser Wert muss 1 oder 2 sein.

</dd> <dt>

*pForm* \[ out\]
</dt> <dd>

Zeiger auf eine oder mehrere [**FORM \_ INFO \_ 1-Strukturen**](form-info-1.md) oder auf eine oder mehrere [**FORM INFO \_ \_ 2-Strukturen.**](form-info-2.md) Alle -Strukturen haben die gleiche Ebene.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Gibt die Größe des Puffers in Bytes an, auf den *pForm* verweist.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die in das Array kopiert wurden, auf das *pForm* verweist (wenn der Vorgang erfolgreich ist) oder die Anzahl der erforderlichen Bytes (wenn ein Fehler auftritt, weil *cbBuf* zu klein ist).

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl von Strukturen empfängt, die in das Array kopiert werden, auf das *pForm* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Wenn der Aufrufer remote und *level* gleich 2 ist, lautet der **StringType-Wert** der zurückgegebenen [**FORM INFO \_ \_ 2-Strukturen**](form-info-2.md) immer **STRING \_ LANGPAIR.**

In Windows Vista werden die von **EnumForms zurückgegebenen** Formulardaten aus einem lokalen Cache abgerufen, wenn *hPrinter* auf einen Remotedruckserver oder einen Drucker verweist, der von einem Druckerserver gehostet wird und mindestens eine offene Verbindung mit einem Drucker auf dem Remotedruckserver besteht. In allen anderen Konfigurationen werden die Formulardaten vom Remotedruckserver abgefragt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumFormsW** (Unicode) und **EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**FORMULARINFORMATIONEN \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




