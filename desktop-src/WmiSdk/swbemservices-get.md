---
description: Ruft ein-Objekt ab, das entweder eine Klassendefinition oder eine-Instanz ist, basierend auf dem Objekt Pfad.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Swap Services. Get-Methode (wbemdisp. h)
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
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349271"
---
# <a name="swbemservicesget-method"></a>Methode "Swap Services. Get"

Mit der **Get** -Methode des-Objekts " [**Swap Services**](swbemservices.md) " wird ein-Objekt abgerufen, das entweder eine Klassendefinition oder eine-Instanz ist, die auf dem Objekt Pfad basiert. Diese Methode ruft nur Objekte aus dem Namespace ab, der dem aktuellen ' **Swap Services** '-Objekt zugeordnet ist.

Die-Methode wird im synchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*strobjectpath* \[ optionale\]
</dt> <dd>

Eine Zeichenfolge, die den Objekt Pfad des abzurufenden-Objekts enthält. Wenn dieser Wert leer ist, kann das leere Objekt, das zurückgegeben wird, eine neue Klasse werden. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten der Abfrage bestimmt. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der [**Vorgang**](swbemobject.md) erfolgreich ist, gibt diese Methode ein-Objekt zurück, das das angeforderte Objekt darstellt.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Get** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Zugriff auf das Objekt.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103a)
</dt> <dd>

Der angegebene Pfad war ungültig.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Objekt wurde nicht gefunden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im Gegensatz zu den Methoden [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) und [**InstancesOf**](swbemservices-instancesof.md) gibt die Get-Methode immer ein- [**Objekt**](swbemobject.md) zurück, das eine bestimmte Instanz einer von WMI verwalteten Ressource darstellt. Zum Abrufen einer bestimmten Instanz einer durch WMI verwalteten Ressource mithilfe der Get-Methode müssen Sie die abzurufende Instanz abrufen, indem Sie die-Methode den Objekt Pfad übergeben, wie im folgenden Skript gezeigt.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Mit dieser Methode können Sie [*Singleton*](gloss-s.md) -Objekte, z. b. [**\_ \_ cimumidentifizierung**](--cimomidentification.md), mit Versionsinformationen zur WMI-Installation, die ausgeführt wird, abrufen.

Sie können das Repository mit einem Anzeige Tool wie [CIM Studio](further-information.md) untersuchen, um zu überprüfen, ob die neue Klasse und Instanz angezeigt werden. Ein Beispiel für das Entfernen einer Klasse und einer Instanz aus dem Repository finden Sie unter " [**errbemservices. Delete**](swbemservices-delete.md) " oder " [**errbemubject. Delete \_**](swbemobject-delete-.md)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> </dl>

 

 




