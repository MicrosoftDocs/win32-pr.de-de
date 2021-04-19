---
description: Mit der Connect-Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Untc:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348157"
---
# <a name="irtcconnect-method"></a>Untc:: Connect-Methode

Mit der **Connect** -Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinputblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen für diese Verbindung.

</dd> <dt>

*Status callbackproc* \[ in\]
</dt> <dd>

Adresse der Status Rückruffunktion des Benutzers, die Statusaktualisierungen (z. b. Trigger) empfängt. Dieser Parameter kann auf **null** festgelegt werden.

</dd> <dt>

*Framescallbackproc* \[ in\]
</dt> <dd>

Adresse der Frame Rückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen (z. b. Trigger) verwendet wird. Dieser Parameter kann auf **null** festgelegt werden.

</dd> <dt>

*UserContext* \[ in\]
</dt> <dd>

Der Wert, der beim Aufrufen des Status und der Frame Rückruffunktion des Benutzers erfolgreich ist. Wenn beide Rückruf Funktionen angegeben werden, muss der gleiche Benutzer Kontextwert verwendet werden. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "This"-Zeiger.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält. Weitere Informationen zu den Funktionen im fehlerblob finden Sie in den Hinweisen am Ende dieses Themas.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich derjenigen, die vom internen " **iritc:: Configure** "-Befehl zurückgegeben werden):



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ bereits \_ verbunden**</dt> </dl>            | Diese Instanz des NPP-com-Objekts ist bereits mit dem Netzwerk verbunden.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt> </dl>       | Das konfigurationsblob ist beschädigt. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt> </dl> | Für das vom *hinputblob* -Parameter angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den " **untc:: Connect** "-oder " **untc:: Configure** "-Befehl generiert werden. Sehen Sie sich den von *herrorblob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt> </dl>        | Die Funktion "| **ateblob** " wurde nicht aufgerufen. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                         |
| <dl> <dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt> </dl>         | Die Zeichenfolge wird nicht mit Null beendet. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**nmerr-Fehler (unzulässig) \_ \_**</dt> </dl>              | Der Auslöse Teil des eingabeblobs ist beschädigt. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                        |
| <dl> <dt>**Ungültiges nmerr- \_ \_ BLOB**</dt> </dl>                 | Das in *hinputblob* angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                      |
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl>               | Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                              |
| <dl> <dt>**nmerr- \_ Timeout**</dt> </dl>                       | Timeout bei der Anforderung. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                                                               |
| <dl> <dt>**nmerr- \_ Uplevel- \_ BLOB**</dt> </dl>                 | Die in *hinputblob* angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn die **Connect** -Methode aufgerufen wird, ruft der NPP die Methode " **untc:: Configure** " automatisch mithilfe des von *hinputblob* bereitgestellten BLOB auf. Beachten Sie, dass alle Fehlercodes, die vom-Befehl an " **untc:: Configure** " zurückgegeben werden, vom " **untc:: Connect** "-Befehl zurückgegeben und zurückgegeben

Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die Schnittstelle " **iritc** " verwenden, um Frames zu erfassen.

Wenn Sie diese Funktion aufrufen, müssen Sie eine Status-oder Frame Rückruffunktion angeben, auch wenn Sie nur als Platzhalter fungiert.

Das von *hinputblob* angegebene Eingabe-BLOB kann durch Aufrufen der Methoden **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.

Das in *herrorblob* zurückgegebene Fehler-BLOB enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann. Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hinputblob* angegebenen eingabeblob nicht verstehen oder finden konnten. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.



| Informationen über                          | Finden Sie unter                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des eingabeblobs, das eine NIC darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

["Iran:: Configure"](irtc-configure.md)
</dt> <dt>

[:D isconnect](irtc-disconnect.md)
</dt> <dt>

["Iran:: Start"](irtc-start.md)
</dt> </dl>

 

 




