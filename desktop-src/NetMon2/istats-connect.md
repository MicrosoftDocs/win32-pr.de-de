---
description: 'IStats::Connect-Methode: Die Connect-Methode verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: IStats::Connect-Methode (Netmon.h)
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
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098478"
---
# <a name="istatsconnect-method"></a>IStats::Connect-Methode

Die **Connect-Methode** verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.

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

*hInputBlob* \[ In\]
</dt> <dd>

Handle für das BLOB, das die NIC angibt, mit der das NPP eine Verbindung herstellt, und die Konfigurationsinformationen für diese Verbindung angibt.

</dd> <dt>

*StatusCallbackProc* \[ In\]
</dt> <dd>

Adresse der Rückruffunktion des Benutzers, die Statusaktualisierungen wie Trigger empfängt. Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *UserContext-Parameter* auf **NULL fest.**

</dd> <dt>

*UserContext* \[ In\]
</dt> <dd>

Wert, der übergeben wird, wenn die Rückruffunktion des Benutzers aufgerufen wird. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein This-Zeiger. Wenn keine Rückruffunktion angegeben wird, legen Sie diesen Parameter und den *StatusCallbackProc-Parameter* auf **NULL fest.**

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle für ein Fehlerblob, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IStats::Configure-Aufruf zurückgegeben** werden):



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
<td>Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>Das Konfigurations-BLOB ist beschädigt. Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Dem durch den <em>hInputBlob-Parameter</em> angegebenen Eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den <strong>Aufruf IStats::Connect</strong> oder <strong>IStats::Configure</strong> generiert werden. Sehen Sie sich den von <em>hErrorBlob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>Die <strong>CreateBlob-Funktion</strong> wurde nicht aufgerufen. Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>Die Zeichenfolge ist nicht NULL-terminiert. Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>Der Triggerteil des Eingabeblobs ist beschädigt. Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>Das in <em>hInputBlob</em> angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>Das Standarderfassungsverzeichnis wurde in der Registrierung nicht festgelegt. Verwenden Sie zum Festlegen des Erfassungsverzeichnisses den folgenden Pfad. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher war nicht verfügbar. Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Für die Anforderung ist ein Time out erfolgt. Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Die In <em>hInputBlob</em> angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn die **Connect-Methode** aufgerufen wird, ruft Netzwerkmonitor **die IStats::Configure-Methode** automatisch auf, indem das vom *hInputBlob-Parameter* bereitgestellte BLOB verwendet wird. Beachten Sie, dass alle Fehlercodes, die durch den Aufruf von **IStats::Configure** zurückgegeben werden, zurückgegeben und vom **IStats::Connect-Aufruf zurückgegeben** werden.

Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können. Beachten Sie, dass Sie beim Herstellen einer Verbindung mit dem Netzwerk mit dieser Methode weiterhin die **IStats-Schnittstelle** verwenden müssen, um Frames zu erfassen.

Das von *hInputBlob* angegebene EingabeBLOB kann durch Aufrufen der **Methoden GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** ermittelt werden.

Das vom *hErrorBlob-Parameter* zurückgegebene FehlerBLOB enthält Einträge, die Netzwerkmonitor in dem in *hInputBlob* angegebenen EingabeBLOB nicht verstehen oder finden konnten. Das zurückgegebene Fehlerblob enthält Fehlerinformationen, die die Anwendung für die Problembehandlung verwenden kann. Wenn beispielsweise NMERR BLOB ENTRY DOES NOT EXIST zurückgegeben wird, wird der Eintrag, den Netzwerkmonitor nicht finden konnte, \_ \_ in das zurückgegebene \_ \_ FehlerBLOB \_ eingeschlossen.



| Informationen über                                             | Finden Sie unter                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des Eingabeblobs, das eine Netzwerkschnittstellenkarte darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::D isconnect](istats-disconnect.md)
</dt> <dt>

[Netzwerkmonitor BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 




