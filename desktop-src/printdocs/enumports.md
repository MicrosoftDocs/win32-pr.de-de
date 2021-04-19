---
description: Die enumports-Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Enumports-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356293"
---
# <a name="enumports-function"></a>Enumports-Funktion

Die **enumports** -Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, dessen Druckerports Sie auflisten möchten.

Wenn *PName* den Wert **null** hat, listet die Funktion die Drucker Anschlüsse des lokalen Computers auf.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationen, die im *pports* -Puffer zurückgegeben werden. Wenn *Level* gleich 1 ist, empfängt *pports* ein Array von [**Port \_ Info \_ 1**](port-info-1.md) -Strukturen. Wenn *Level* gleich 2 ist, empfängt *pports* ein Array von [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen.

</dd> <dt>

*pports* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**Port \_ Info \_ 1**](port-info-1.md) -oder [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen empfängt. Jede Struktur enthält Daten, die einen verfügbaren Druckerport beschreiben. Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.

Um die erforderliche Puffergröße zu ermitteln, nennen Sie **enumports** , bei denen *cbbuf* auf NULL festgelegt ist. **Enumports** schlagen fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pports* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pports* -Puffer kopiert werden. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von [**Port \_ Info \_ 1**](port-info-1.md) -oder [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen empfängt, die im *pports* -Puffer zurückgegeben werden. Dies ist die Anzahl der Drucker Anschlüsse, die auf dem angegebenen Server verfügbar sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die **enumports** -Funktion kann auch dann erfolgreich ausgeführt werden, wenn der durch *PName* angegebene Server keinen Drucker definiert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumportsw** (Unicode) und **enumportsa** (ANSI)<br/>                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**Port \_ Info \_ 1**](port-info-1.md)
</dt> <dt>

[**Port \_ Info \_ 2**](port-info-2.md)
</dt> </dl>

 

