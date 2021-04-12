---
description: Die Funktion deletePort zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: DeletePort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216873"
---
# <a name="deleteport-function"></a>DeletePort-Funktion

Die Funktion **deletePort** zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endende Zeichenfolge, die den Namen des Servers angibt, für den der Port gelöscht werden soll. Wenn dieser Parameter **null** ist, wird ein lokaler Port gelöscht.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Dialog Felds zum Löschen von Port.

</dd> <dt>

*pportname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endende Zeichenfolge, die den Namen des Ports angibt, der gelöscht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Eine Anwendung kann die Namen gültiger Ports abrufen, indem die [**enumports**](enumports.md) -Funktion aufgerufen wird.

Die **deletePort** -Funktion gibt einen Fehler zurück, wenn zurzeit ein Drucker mit dem angegebenen Port verbunden ist.

Der Aufrufer der **deletePort** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteportw** (Unicode) und **deleteporta** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




