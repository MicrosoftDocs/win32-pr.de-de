---
description: Ruft ein Objekt ab, bei dem es sich entweder um eine Klassendefinition oder eine Instanz handelt, basierend auf dem Objektpfad.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: SWbemServices.Get-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312659"
---
# <a name="swbemservicesget-method"></a>SWbemServices.Get-Methode

Die **Get-Methode** des [**SWbemServices-Objekts**](swbemservices.md) ruft basierend auf dem Objektpfad ein Objekt ab, das entweder eine Klassendefinition oder eine Instanz ist. Diese Methode ruft nur Objekte aus dem Namespace ab, der dem aktuellen **SWbemServices-Objekt** zugeordnet ist.

Die -Methode wird im synchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strObjectPath* \[ Optional\]
</dt> <dd>

Zeichenfolge, die den Objektpfad des abzurufende Objekts enthält. Wenn dieser Wert leer ist, kann das leere Objekt, das zurückgegeben wird, zu einer neuen Klasse werden. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Ganze Zahl, die das Verhalten der Abfrage bestimmt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers( (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurückgibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode ein [**SWbemObject-Objekt**](swbemobject.md) zurück, das das angeforderte Objekt darstellt.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Get-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Zugriff auf das Objekt.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrInvalidObjectPath** – 2147749946 (0x8004103A)
</dt> <dd>

Der angegebene Pfad war ungültig.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Objekt konnte nicht gefunden werden.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im Gegensatz zu den [**Methoden ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) und [**InstancesOf**](swbemservices-instancesof.md) gibt die Get-Methode immer ein [**SWbemObject**](swbemobject.md) zurück, das eine bestimmte Instanz einer von WMI verwalteten Ressource darstellt. Um eine bestimmte Instanz einer von WMI verwalteten Ressource mithilfe der Get-Methode abzurufen, müssen Sie get the instance to retrieve anzuweisen, indem Sie der Methode den Objektpfad übergeben, wie im folgenden Skript gezeigt.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Sie können diese Methode verwenden, um [*Singletonobjekte*](gloss-s.md) wie [**\_ \_ CIMOMIdentification**](--cimomidentification.md)abzurufen, die Versionsinformationen zur ausgeführten WMI-Installation enthalten.

Sie können das Repository mit einem Anzeigetool wie [CIM Studio](further-information.md) untersuchen, um zu überprüfen, ob die neue Klasse und Instanz angezeigt werden. Ein Beispiel für das Entfernen einer Klasse und instanz aus dem Repository finden Sie unter [**SWbemServices.Delete**](swbemservices-delete.md) oder [**SWbemObject.Delete. \_**](swbemobject-delete-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**Swbemobject**](swbemobject.md)
</dt> </dl>

 

 




