---
description: Die Funktion enumprintprozessoren listet die auf dem angegebenen Server installierten Druck Prozessoren auf.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Enumprintprocessor-Funktion (winspool. h)
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
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960089"
---
# <a name="enumprintprocessors-function"></a>Enumprintprozessoren-Funktion

Die Funktion **enumprintprozessoren** listet die auf dem angegebenen Server installierten Druck Prozessoren auf.

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich die Druck Prozessoren befinden. Wenn dieser Parameter **null** ist, werden die lokalen Druck Prozessoren aufgezählt.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationen, die im *pprintprocessorinfo* -Puffer zurückgegeben werden. Dieser Parameter muss 1 sein.

</dd> <dt>

*pprintprocessorinfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**PrintProcessor \_ Info \_ 1**](printprocessor-info-1.md) -Strukturen empfängt. Jede Struktur beschreibt einen verfügbaren Druck Prozessor. Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen zu erhalten, auf die die Strukturmember zeigen.

Um die erforderliche Puffergröße zu ermitteln, muss **enumprintprocessor** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist. **Enumprintprocessor** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pprintprocessorinfo* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pprintprocessorinfo* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pprintprocessorinfo* -Puffer zurückgegebenen Strukturen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumprintprocessorsw** (Unicode) und **enumprintprocessorsa** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprintprocessor**](addprintprocessor.md)
</dt> <dt>

[**Enumprintprocessordatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**PrintProcessor \_ Info \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

