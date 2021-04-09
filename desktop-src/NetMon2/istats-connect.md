---
description: Mit der Connect-Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStats:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869236"
---
# <a name="istatsconnect-method"></a>IStats:: Connect-Methode

Mit der **Connect** -Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.

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

Handle für das BLOB, das die NIC angibt, mit der der NPP eine Verbindung herstellt, und die Konfigurationsinformationen für diese Verbindung.

</dd> <dt>

*Status callbackproc* \[ in\]
</dt> <dd>

Adresse der Rückruffunktion des Benutzers, die Statusaktualisierungen (z. b. Trigger) empfängt. Wenn eine Rückruffunktion nicht verwendet wird, legen Sie diesen Parameter und den *userContext* -Parameter auf **null** fest.

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

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, handelt es sich bei dem Rückgabewert um einen der folgenden Fehlercodes (einschließlich der vom internen **iStats:: Configure** -Befehl zurückgegebenen Fehler):



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
<td>Das konfigurationsblob ist beschädigt. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Für das vom <em>hinputblob</em> -Parameter angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den <strong>iStats:: Connect</strong> -oder <strong>iStats:: Configure</strong> -Befehl generiert werden. Sehen Sie sich den von <em>herrorblob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>Die Funktion "| <strong>ateblob</strong> " wurde nicht aufgerufen. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>Die Zeichenfolge wird nicht mit Null beendet. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>Der Auslöse Teil des eingabeblobs ist beschädigt. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>Das in <em>hinputblob</em> angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>Das Standard Erfassungs Verzeichnis wurde nicht in der Registrierung festgelegt. Verwenden Sie den folgenden Pfad, um das Erfassungs Verzeichnis festzulegen. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher war nicht verfügbar. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Timeout bei der Anforderung. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Die in <em>hinputblob</em> angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den <strong>iStats:: Configure</strong> -Befehl generiert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn die **Connect** -Methode aufgerufen wird, ruft Netzwerkmonitor automatisch die **iStats:: Configure** -Methode auf, indem das BLOB verwendet wird, das vom *hinputblob* -Parameter bereitgestellt wird. Beachten Sie, dass alle Fehlercodes, die vom iStats:: **configure** -Befehl zurückgegeben werden, zurückgegeben und vom **iStats:: Connect** -Befehl zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie die **iStats** -Schnittstelle weiterhin verwenden, um Frames zu erfassen.

Das von *hinputblob* angegebene Eingabe-BLOB kann durch Aufrufen der Methoden **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.

Das vom " *herrorblob* "-Parameter zurückgegebene Fehler-BLOB enthält Einträge, die Netzwerkmonitor in dem in *hinputblob* angegebenen eingabeblob nicht verstehen oder finden konnten. Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag, den Netzwerkmonitor nicht finden konnte, in das zurückgegebene fehlerblob eingefügt.



| Informationen über                                             | Finden Sie unter                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des eingabeblobs, das eine Netzwerkschnittstellenkarte darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Configure](istats-configure.md)
</dt> <dt>

[IStats::D isconnect](istats-disconnect.md)
</dt> <dt>

[BlobNetzwerkmonitor](network-monitor-blobs.md)
</dt> </dl>

 

 




