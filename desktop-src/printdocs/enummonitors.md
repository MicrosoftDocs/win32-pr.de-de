---
description: Die enummonitors-Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Enummonitors-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756402"
---
# <a name="enummonitors-function"></a>Enummonitors-Funktion

Die **enummonitors** -Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich die Monitore befinden. Wenn dieser Parameter **null** ist, werden die lokalen Monitore aufgezählt.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der Struktur, auf die von *pmonitors* verwiesen wird.

Dieser Wert kann 1 oder 2 sein.

</dd> <dt>

*pmonitors* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von-Strukturen empfängt. Der Puffer muss groß genug sein, um die von den Strukturmembern referenzierten Zeichen folgen zu speichern.

Um die erforderliche Puffergröße zu ermitteln, müssen Sie **enummonitors** mit der Festlegung von *cbbuf* auf NULL aufzurufen. " **Enummonitors** " schlägt fehl, " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

Der Puffer erhält ein Array von [**Monitor \_ Info \_ 1**](monitor-info-1.md) -Strukturen, wenn die *Ebene* 1 ist, oder [**Monitor \_ Info \_ 2**](monitor-info-2.md) -Strukturen, wenn die *Ebene* 2 ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pmonitors* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Strukturen erhält, die im Puffer zurückgegeben wurden, auf den *pmonitors* zeigt.

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
| Unicode- und ANSI-Name<br/>   | **Enummonitorsw** (Unicode) und **enummonitorsa** (ANSI)<br/>                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Überwachen von \_ Informationen \_ 1**](monitor-info-1.md)
</dt> <dt>

[**Überwachen von \_ Informationen \_ 2**](monitor-info-2.md)
</dt> </dl>

 

