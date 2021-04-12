---
description: Die enumprintprocessordatatypes-Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Enumprintprocessordatatypes-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529000"
---
# <a name="enumprintprocessordatatypes-function"></a>Enumprintprocessordatatypes-Funktion

Die **enumprintprocessordatatypes** -Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich der Druck Prozessor befindet. Wenn dieser Parameter **null** ist, werden die Datentypen für den lokalen Druck Prozessor aufgezählt.

</dd> <dt>

*pprintprocessorname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druck Prozessors angibt, dessen Datentypen aufgelistet werden.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationen, die im Puffer *pdatatypes* zurückgegeben werden. Dieser Parameter muss 1 sein.

</dd> <dt>

*pdatatypes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**Datatypes- \_ Informationen \_ 1**](datatypes-info-1.md) -Strukturen empfängt. Jede Struktur beschreibt einen verfügbaren Datentyp. Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.

Um die erforderliche Puffergröße zu ermitteln, müssen Sie **enumprintprocessordatatypes** aufrufen, wobei *cbbuf* auf 0 (null) festgelegt ist. **Enumprintprocessordatatypes** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pdatatypes* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pdatatypes* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pdatatypes* -Puffer zurückgegebenen Strukturen empfängt. Dies ist die Anzahl der unterstützten Datentypen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

v

Ab Windows Vista werden die Datentyp Informationen von Remote Druckservern aus einem lokalen Cache abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumprintprocessordatatypesw** (Unicode) und **enumprintprocessordatatypesa** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Datatypes- \_ Informationen \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**Enumprintprozessoren**](enumprintprocessors.md)
</dt> </dl>

 

