---
description: Das onobjectready-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner Vorgang ein Objekt zurückgibt.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onobjectready-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130961"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>Iswbemsinkevents:: onobjectready-Ereignis

Das **onobjectready** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner Vorgang ein Objekt zurückgibt. Verwenden Sie dieses Ereignis, um Objekte aus asynchronen Aufrufen wie z. [**b. "slibemubject \_ . instancesasync**](swbemobject-instancesasync-.md) " oder " [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md)" zu verarbeiten. **Onobjectready** gibt jedes Mal ein [**Austausch Objekt**](swbemobject.md) zurück, bis die Enumeration beendet ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemujekt* 
</dt> <dd>

Ein-Objekt mit einem [**Swap**](swbemobject.md) -Objekt. Dies ähnelt dem, was vom synchronen Äquivalent des asynchronen Aufrufes zurückgegeben wird, der dieses Ereignis auslöst. Beispielsweise gibt ein Aufrufen der Methode " [**errbemservices. getasync**](swbemservices-getasync.md) " ein " **errbewbject** " *im objwbefubject* -Parameter des " **onobjectready** "-Ereignisses des " [**slibemsink**](swbemsink.md) "-Objekts zurück, das als *objwbefubject* -Parameter des ursprünglichen Aufrufes-Objekts übergeben wird. Das gleiche " **errbejebject** "-Objekt kann mithilfe eines äquivalenten synchronen Aufrufes für " [**errbemservices. Get**](swbemservices-get.md)" abgerufen werden.

</dd> <dt>

*objwbemasynccontext* 
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird. Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss des **onobjectready** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.

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

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

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

 

