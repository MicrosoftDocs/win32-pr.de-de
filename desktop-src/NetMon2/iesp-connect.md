---
description: Die Verbinden-Methode verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen über die Verbindung bereit.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: IESP::Verbinden-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9383b6d7638df89bebd369a3657283c1fd6b56ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480146"
---
# <a name="iespconnect-method"></a>IESP::Verbinden-Methode

Die **Verbinden-Methode** verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen über die Verbindung bereit.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hInputBlob* \[ In\]
</dt> <dd>

Handle für das BLOB, das die NIC angibt, mit der das NPP eine Verbindung herstellt, und die Konfigurationsinformationen für diese Verbindung.

</dd> <dt>

*StatusCallbackProc* \[ In\]
</dt> <dd>

Adresse der Rückruffunktion des Benutzers, die Statusupdates wie Trigger empfängt. Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *UserContext-Parameter* auf **NULL** fest.

</dd> <dt>

*UserContext* \[ In\]
</dt> <dd>

Wert, der übergeben wird, wenn die Rückruffunktion des Benutzers aufgerufen wird. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "this"-Zeiger. Wenn keine Rückruffunktion angegeben ist, legen Sie diesen Parameter und den *StatusCallbackProc-Parameter* auf **NULL** fest.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Behandeln sie ein Fehler-BLOB, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IESP::Configure-Aufruf** zurückgegeben werden):




| Rückgabecode | Beschreibung | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | Das Konfigurations-BLOB ist beschädigt. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | Dem durch den <em>hInputBlob-Parameter</em> angegebenen Eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den <strong>IESP::Verbinden-</strong> oder <strong>IESP::Configure-Aufruf</strong> generiert werden. Sehen Sie sich den von <em>hErrorBlob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | Die <strong>CreateBlob-Funktion</strong> wurde nicht aufgerufen. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | Die Zeichenfolge ist nicht NULL-terminiert. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | Der Triggerteil des Eingabeblobs ist beschädigt. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | Das in <em>hInputBlob</em> angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | Das Standarderfassungsverzeichnis wurde in der Registrierung nicht festgelegt. Verwenden Sie den folgenden Pfad, um das Erfassungsverzeichnis festzulegen. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Für die Anforderung ist ein Time out aufgetreten. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | Die in <em>hInputBlob</em> angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den <strong>IESP::Configure-Aufruf</strong> generiert.<br /> | 




 

## <a name="remarks"></a>Hinweise

Wenn die **Verbinden-Methode** aufgerufen wird, ruft Netzwerkmonitor automatisch **IESP::Configure** auf, indem das vom *hInputBlob-Parameter* bereitgestellte BLOB verwendet wird. Beachten Sie, dass alle Fehlercodes, die vom Aufruf von **IESP::Configure** zurückgegeben werden, vom **IESP::Verbinden-Aufruf** zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit der Erfassung von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mit dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die **IESP-Schnittstelle** verwenden, um Frames zu erfassen.

Das von *hInputBlob* angegebene Eingabe-BLOB kann durch Aufrufen von **GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** abgerufen werden.

Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Eingabe-BLOB finden konnten, das in *hInputBlob* angegeben ist. Das zurückgegebene Fehler-BLOB enthält Fehlerinformationen, die die Anwendung für die Problembehandlung verwenden kann. Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnten, im zurückgegebenen Fehlerblob enthalten.



| Informationen über                          | Finden Sie unter                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des Eingabeblobs, das eine NIC darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Configure](iesp-configure.md)
</dt> <dt>

[IESP::D isconnect](iesp-disconnect.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> </dl>

 

 




