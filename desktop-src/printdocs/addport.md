---
description: Die AddPort-Funktion fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die AddPort-Funktion wird vom Portmonitor exportiert.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: AddPort-Funktion (Winspool.h)
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
ms.openlocfilehash: abbb2e4b836c64ddff47c92681e32bd0d5f9f0c38224d6c710fb10bc3435ac96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112690"
---
# <a name="addport-function"></a>AddPort-Funktion

Die **AddPort-Funktion** fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die **AddPort-Funktion** wird vom Portmonitor exportiert.

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

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den Namen des Servers angibt, mit dem der Port verbunden ist. Wenn dieser Parameter **NULL ist,** ist der Port lokal.

</dd> <dt>

*hWnd* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des **Dialogfelds AddPort.**

</dd> <dt>

*pMonitorName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den monitor angibt, der dem Port zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die **AddPort-Funktion** durchsucht das Netzwerk, um nach vorhandenen Ports zu suchen, und zeigt ein Dialogfeld für den Benutzer an. Die **AddPort-Funktion** sollte den vom Benutzer eingegebenen Portnamen überprüfen, indem [**sie EnumPorts**](enumports.md) aufruft, um sicherzustellen, dass keine doppelten Namen vorhanden sind.

Der Aufrufer der **AddPort-Funktion** muss über SERVER ACCESS ADMINISTER-Zugriff auf den Server verfügen, \_ mit dem der Port verbunden \_ ist.

Um einen Port hinzuzufügen, ohne ein Dialogfeld anzuzeigen, rufen Sie die **XcvData-Funktion** anstelle von **AddPort auf.** Weitere Informationen zu **XcvData finden** Sie im Microsoft Windows Driver Development Kit (DDK).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **AddPortW** (Unicode) und **AddPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Weitere Informationen

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

 

 




