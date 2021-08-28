---
description: Die EnumPrintProcessors-Funktion enumPrintProcessors enumeriert die auf dem angegebenen Server installierten Druckprozessoren.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: EnumPrintProcessors-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 800ed5afcf332a0c34dc272158f98fed64e47e86cb3c16cb24d6013951ffd3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846040"
---
# <a name="enumprintprocessors-function"></a>EnumPrintProcessors-Funktion

Die **EnumPrintProcessors-Funktion** aufzählt die Druckprozessoren, die auf dem angegebenen Server installiert sind.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Servers angibt, auf dem sich die Druckprozessoren befinden. Wenn dieser Parameter **NULL ist,** werden die lokalen Druckprozessoren aufzählt.

</dd> <dt>

*pUmgebung* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL ist,** wird die aktuelle Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) verwendet.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Typ der im *pPrintProcessorInfo-Puffer zurückgegebenen* Informationen. Dieser Parameter muss 1 sein.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**PRINTPROCESSOR \_ INFO \_ 1-Strukturen**](printprocessor-info-1.md) empfängt. Jede -Struktur beschreibt einen verfügbaren Druckprozessor. Der Puffer muss groß genug sein, um das Array von Strukturen und alle Zeichenfolgen zu empfangen, auf die die Strukturmitglieder zeigen.

Um die erforderliche Puffergröße zu bestimmen, rufen Sie **EnumPrintProcessors** mit *cbBuf* auf 0 (null) auf. **Bei EnumPrintProcessors** tritt ein Fehler auf, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR INSUFFICIENT BUFFER zurück, und der \_ parameter \_ *"arraysNeeded"* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pPrintProcessorInfo zeigt.*

</dd> <dt>

*-Needed* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der in den *pPrintProcessorInfo-Puffer* kopierten Bytes empfängt, wenn die Funktion erfolgreich ist. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable empfängt die erforderliche Anzahl von Bytes.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pPrintProcessorInfo-Puffer* zurückgegebenen Strukturen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumPrintProcessorsW** (Unicode) und **EnumPrintProcessorsA** (ANSI)<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**PRINTPROCESSOR \_ INFO \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

