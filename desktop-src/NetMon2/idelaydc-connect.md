---
description: Die Verbinden-Methode verbindet das NPP mithilfe einer angegebenen Netzwerkschnittstellenkarte mit dem Netzwerk und stellt Konfigurationsinformationen zur Verbindung bereit.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: IDelaydC::Verbinden-Methode (Netmon.h)
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
ms.openlocfilehash: e91db1dae0c67c5f35e46841867d3d3e15058cf0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477305"
---
# <a name="idelaydcconnect-method"></a>IDelaydC::Verbinden-Methode

Die **Verbinden-Methode** verbindet das NPP mithilfe einer angegebenen Netzwerkschnittstellenkarte mit dem Netzwerk und stellt Konfigurationsinformationen über die Verbindung bereit.

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

Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen zu dieser Verbindung.

</dd> <dt>

*StatusCallbackProc* \[ In\]
</dt> <dd>

Adresse der Rückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen wie Triggern verwendet wird. Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *UserContext-Parameter* auf **NULL** fest.

</dd> <dt>

*UserContext* \[ In\]
</dt> <dd>

Wert, der übergeben wird, wenn die Rückruffunktion des Benutzers aufgerufen wird. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "this"-Zeiger. Wenn keine Rückruffunktion angegeben ist, legen Sie diesen Parameter und den *StatusCallbackProc-Parameter* auf **NULL** fest.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Behandeln sie ein Fehlerblob, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IDelaydC::Configure-Aufruf** zurückgegeben werden):




| Rückgabecode | Beschreibung | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | Das Konfigurations-BLOB ist beschädigt. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | Dem von <em>hInputBlob</em> angegebenen Eingabe-BLOB fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den Aufruf von <strong>IDelaydC::Verbinden</strong> oder <strong>IDelaydC::Configure</strong> generiert werden. Sehen Sie sich den von <em>hErrorBlob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | Die <strong>CreateBlob-Funktion</strong> wurde nicht aufgerufen. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | Die Zeichenfolge ist nicht NULL-terminiert. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | Der Triggerteil des Eingabeblobs ist beschädigt. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | Das in <em>hInputBlob</em> angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | Das Standarderfassungsverzeichnis wurde in der Registrierung nicht festgelegt. Verwenden Sie den folgenden Pfad, um das Erfassungsverzeichnis festzulegen. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | Für diesen Vorgang war kein Arbeitsspeicher verfügbar. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Für die Anforderung ist ein Time out aufgetreten. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | Die In <em>hInputBlob</em> angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den <strong>IDelaydC::Configure-Aufruf</strong> generiert.<br /> | 




 

## <a name="remarks"></a>Hinweise

Wenn die **Verbinden-Methode** aufgerufen wird, ruft das NPP automatisch **IDelaydC::Configure** auf, indem das von *hInputBlob* bereitgestellte BLOB verwendet wird. Beachten Sie, dass alle Fehlercodes, die durch den Aufruf von **IDelaydC::Configure** zurückgegeben werden, vom **IDelaydC::Verbinden-Aufruf** zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit der Erfassung von Frames beginnen können. Beachten Sie, dass Sie beim Herstellen einer Verbindung mit dem Netzwerk mit dieser Methode weiterhin die **IDelaydC-Schnittstellenmethoden** zum Erfassen von Frames verwenden müssen.

Das durch den *Parameter hInputBlob* angegebene Eingabe-BLOB kann abgerufen werden, indem **GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** aufgerufen werden.

Das in *hErrorBlob* zurückgegebene Fehlerblob enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann. Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Eingabe-BLOB finden konnten, das in *hInputBlob* angegeben ist. Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnte, im zurückgegebenen Fehlerblob enthalten.



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

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> </dl>

 

 




