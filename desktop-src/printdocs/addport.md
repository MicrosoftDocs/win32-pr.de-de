---
description: Die Funktion AddPort fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die Funktion AddPort wird vom Port Monitor exportiert.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: AddPort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868344"
---
# <a name="addport-function"></a>AddPort-Funktion

Die Funktion **AddPort** fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die Funktion **AddPort** wird vom Port Monitor exportiert.

## <a name="syntax"></a>Syntax


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, mit dem der Port verbunden ist. Wenn dieser Parameter **null** ist, ist der Port local.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Dialog Felds **AddPort** .

</dd> <dt>

*pmonitorname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den dem Port zugeordneten Monitor angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die **AddPort** -Funktion durchsucht das Netzwerk, um vorhandene Ports zu suchen, und zeigt ein Dialogfeld für den Benutzer an. Die **AddPort** -Funktion muss den vom Benutzer eingegebenen Portnamen durch Aufrufen von [**enumports**](enumports.md) überprüfen, um sicherzustellen, dass keine doppelten Namen vorhanden sind.

Der Aufrufer der **AddPort** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.

Um einen Port hinzuzufügen, ohne ein Dialogfeld anzuzeigen, müssen Sie die **XcvData** -Funktion anstelle von **AddPort** aufzurufen. Weitere Informationen zu **XcvData** finden Sie im Microsoft Windows Driver Development Kit (DDK).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **Addportw** (Unicode) und **addporta** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




