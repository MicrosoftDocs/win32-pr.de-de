---
description: Die deleteprinterdriver-Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Deleteprinterdriver-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363441"
---
# <a name="deleteprinterdriver-function"></a>Deleteprinterdriver-Funktion

Die **deleteprinterdriver** -Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.

Um die dem Treiber zugeordneten Dateien zu löschen und den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber für einen Server zu entfernen, verwenden Sie die Funktion [**deleteprinterdriverex**](deleteprinterdriverex.md) .

**Deleteprinterdriver** löscht einen Treiber nur dann, wenn keine Version des Treibers für die angegebene Umgebung verwendet wird. [**Deleteprinterdriverex**](deleteprinterdriverex.md) kann bestimmte Versionen des Treibers löschen.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll. Wenn dieser Parameter **null** ist, wird der Name des Druckertreibers lokal entfernt.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird der Treiber Name aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) gelöscht.

</dd> <dt>

*pdrivername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Treibers angibt, der gelöscht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Die **deleteprinterdriver** -Funktion löscht die zugeordneten Dateien nicht, sondern entfernt lediglich den Treiber Namen aus der Liste, die von der [**enumprinterdrivers**](enumprinterdrivers.md) -Funktion zurückgegeben wird.

Vor dem Aufrufen von **deleteprinterdriver** müssen Sie alle Drucker Objekte löschen, die den Druckertreiber verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteprinterdriverw** (Unicode) und **deleteprinterdrivera** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterdriverex**](deleteprinterdriverex.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> </dl>

 

