---
description: Die SetPort-Funktion legt den einem Druckerport zugeordneten Status fest.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: SetPort-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e3414d0566203aa51d78c6b7d4b0463cee5765bae8c35c083a959088b6559df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234030"
---
# <a name="setport-function"></a>SetPort-Funktion

Die **SetPort-Funktion** legt den einem Druckerport zugeordneten Status fest.

## <a name="syntax"></a>Syntax


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den Namen des Druckerservers angibt, mit dem der Anschluss verbunden ist. Legen Sie diesen Parameter auf **NULL** fest, wenn sich der Port auf dem lokalen Computer befindet.

</dd> <dt>

*pPortName* \[ In\]
</dt> <dd>

Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den Namen des Druckerports angibt.

</dd> <dt>

*dwLevel* \[ In\]
</dt> <dd>

Gibt den Typ der Struktur an, auf die der *pPortInfo-Parameter* zeigt.

Dieser Wert muss 3 sein, was einer [**PORT \_ INFO \_ 3-Datenstruktur**](port-info-3.md) entspricht.

</dd> <dt>

*pPortInfo* \[ In\]
</dt> <dd>

Zeiger auf eine [**PORT \_ INFO \_ 3-Struktur,**](port-info-3.md) die die festgelegten Portstatusinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu kommen, dass die Anwendung nicht reagiert.

 

Der Aufrufer der **SetPort-Funktion** muss als Administrator ausgeführt werden. Wenn der Aufrufer ein Portmonitor oder Sprachmonitor ist, muss er [**außerdem RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufrufen, um den Identitätswechsel zu beendet, bevor **SetPort aufruft.**

Alle Programme, die **SetPort aufrufen,** müssen über SERVER ACCESS ADMINISTER-Zugriff auf den Server \_ \_ verfügen, mit dem der Port verbunden ist.

Wenn Sie einen Druckerportstatuswert mit dem Schweregrad PORT STATUS TYPE ERROR festlegen, beendet der Druckspooler das Senden von Aufträgen \_ \_ an den \_ Port. Der Druckspooler setzt das Senden von Aufträgen an den Port wieder ein, wenn der Portstatus durch einen anderen Aufruf von **SetPort entfernt wird.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **SetPortW** (Unicode) und **SetPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**PORTINFORMATIONEN \_ \_ 3**](port-info-3.md)
</dt> </dl>

 

