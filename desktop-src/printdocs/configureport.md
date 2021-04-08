---
description: Die Funktion "Konfigurations Bericht" zeigt das Dialogfeld Port-Konfiguration für einen Port auf dem angegebenen Server an.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Funktion "Konfiguration Report" (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959703"
---
# <a name="configureport-function"></a>Funktion "Konfigurations Bericht"

Die Funktion " **Konfigurations Bericht** " zeigt das Dialogfeld Port-Konfiguration für einen Port auf dem angegebenen Server an.

## <a name="syntax"></a>Syntax


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers angibt, auf dem der angegebene Port vorhanden ist. Wenn dieser Parameter **null** ist, ist der Port local.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle für das übergeordnete Fenster des Dialog Felds Port-Konfiguration.

</dd> <dt>

*pportname* \[ in\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu konfigurierenden Ports angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Vor dem Aufrufen der Funktion " **Konfigurations Bericht** " sollte eine Anwendung die Funktion " [**enumports**](enumports.md) " aufrufen, um gültige Portnamen zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | " **Konfiguriertem Report w** (Unicode)" und " **konfigurier konfigurieren** " (ANSI)<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




