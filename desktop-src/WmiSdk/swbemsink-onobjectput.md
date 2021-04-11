---
description: Das onobjectput-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist. Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onobjectput-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218480"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>Iswbemsinkevents:: onobjectput-Ereignis

Das **onobjectput** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist. Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbefubjectpath* 
</dt> <dd>

Ein Objekt vom Typ " [**errbemubjectpath**](swbemobjectpath.md) ", das den Objekt Pfad der Instanz oder Klasse enthält, die der Put-Vorgang in WMI schreibt.

</dd> <dt>

*objwbemasynccontext* 
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird. Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss des **onobjectput** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Netzwerkfehler. der normale Betrieb wird verhindert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-senbemsink<br/>                                                             |
| IID<br/>                      | IID \_ iswbemsinkevents<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Senke**](swbemsink.md)
</dt> </dl>

 

