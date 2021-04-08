---
description: Mit der Connect-Methode wird die NPP über eine angegebene Netzwerkschnittstellenkarte mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'Idelta-DC:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861999"
---
# <a name="idelaydcconnect-method"></a>Idelta aydc:: Connect-Methode

Mit der **Connect** -Methode wird die NPP über eine angegebene Netzwerkschnittstellenkarte mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinputblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen über diese Verbindung.

</dd> <dt>

*Status callbackproc* \[ in\]
</dt> <dd>

Adresse der Rückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen (z. b. Trigger) verwendet wird. Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *userContext* -Parameter auf **null** fest.

</dd> <dt>

*UserContext* \[ in\]
</dt> <dd>

Der Wert, der beim Aufrufen der Rückruffunktion des Benutzers erfolgreich ist. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "This"-Zeiger. Wenn keine Rückruffunktion angegeben ist, legen Sie diesen Parameter und den Parameter " *Status callbackproc* " auf **null** fest.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **idelta-DC:: Configure** -Befehl zurückgegeben werden):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </dl></td>
<td>Diese Instanz des NPP-com-Objekts ist bereits mit dem Netzwerk verbunden.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>Das konfigurationsblob ist beschädigt. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Für das von <em>hinputblob</em> angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann vom <strong>idelta-DC:: Connect</strong> -oder <strong>idelta-DC:: Configure</strong> -Befehl generiert werden. Sehen Sie sich den von <em>herrorblob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>Die Funktion "| <strong>ateblob</strong> " wurde nicht aufgerufen. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>Die Zeichenfolge wird nicht mit Null beendet. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>Der Auslöse Teil des eingabeblobs ist beschädigt. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>Das in <em>hinputblob</em> angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>Das Standard Erfassungs Verzeichnis wurde nicht in der Registrierung festgelegt. Verwenden Sie den folgenden Pfad, um das Erfassungs Verzeichnis festzulegen. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>Es war kein Arbeitsspeicher verfügbar, um diesen Vorgang auszuführen. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Timeout bei der Anforderung. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Die in <em>hinputblob</em> angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn die **Connect** -Methode aufgerufen wird, ruft der NPP automatisch **idelta-DC:: Configure** mithilfe des BLOBs auf, das von *hinputblob* bereitgestellt wird. Beachten Sie, dass alle Fehlercodes, die vom idelta- **DC:: Configure** -Befehl zurückgegeben werden, zurückgegeben und vom **idelta-DC:: Connect** -Befehl zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie die **idelta-DC** -Schnittstellen Methoden weiterhin verwenden, um Frames zu erfassen.

Der durch den *hinputblob* -Parameter angegebene eingabeblob kann durch Aufrufen von **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.

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

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Configure](idelaydc-configure.md)
</dt> <dt>

[Idelta aydc::D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[Idelta aydc:: Start](idelaydc-start.md)
</dt> </dl>

 

 




