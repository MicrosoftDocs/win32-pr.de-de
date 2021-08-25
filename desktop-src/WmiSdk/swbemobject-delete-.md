---
description: Die \_ Delete-Methode des SWbemObject-Objekts löscht entweder die aktuelle Klasse oder die aktuelle Instanz.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: SWbemObject.Delete_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: db8df81e56db9967db46b88c0587af9b82a6281e7e732b8647059e8bf4f5457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857380"
---
# <a name="swbemobjectdelete_-method"></a>SWbemObject.Delete-Methode \_

Die **\_ Delete-Methode** des [**SWbemObject-Objekts**](swbemobject.md) löscht entweder die aktuelle Klasse oder die aktuelle Instanz. Wenn ein dynamischer Anbieter die Klasse oder Instanz liefert, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen. Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist in der Regel nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Delete-Methode \_** kann **das Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Kontext verfügt nicht über ausreichende Sicherheitsrechte zum Löschen des Objekts.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrInvalidOperation** – 2147749910 (0x80041016)
</dt> <dd>

Das Objekt kann nicht gelöscht werden.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das Objekt war nicht vorhanden.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ Delete-Methode** schlägt fehl, wenn eine neue Instanz von [**SWbemObject**](swbemobject.md) erstellt wird, aber kein Wert für die Schlüsseleigenschaft angegeben wird. Windows Die Verwaltungsinstrumentation (WMI) generiert automatisch einen GUID-Wert (Globally Unique Identifier), aber ein GUID-Wert wird von **SWbemObject.Delete nicht akzeptiert. \_** In diesem Fall funktioniert [**SWbemServices.Delete,**](swbemservices-delete.md)das den Objektpfad verwendet. Beachten Sie, [**dass ein SWbemObjectPath-Objekt**](swbemobjectpath.md) von der [**SWbemObject.Put-Methode \_**](swbemobject-put-.md) zurückgegeben wird, nachdem ein Objekt an WMI gebunden wurde.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine neue Klasse erstellt. fügt eine Schlüsseleigenschaft hinzu. schreibt die neue Klasse in das Repository. und zeigt den Pfad des neuen Klassenobjekts an. Das Skript erstellt dann eine Instanz der neuen -Klasse. schreibt es. und zeigt den Pfad an. Beachten Sie, dass das Skript sowohl die -Klasse als auch die -Instanzen aus dem Repository löscht, indem einfach die -Klasse gelöscht wird.


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




