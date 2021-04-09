---
description: Die Delete- \_ Methode des-Objekts von "Swap" löscht entweder die aktuelle Klasse oder die aktuelle Instanz.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: SWbemObject.Delete_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042585"
---
# <a name="swbemobjectdelete_-method"></a>Errbemubject. Delete- \_ Methode

Die **Delete \_** -Methode des-Objekts von " [**Swap**](swbemobject.md) " löscht entweder die aktuelle Klasse oder die aktuelle Instanz. Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen. Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Delete \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Kontext verfügt nicht über die erforderlichen Sicherheitsrechte, um das Objekt zu löschen.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Das Objekt kann nicht gelöscht werden.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das Objekt ist nicht vorhanden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei **der \_ Delete** -Methode tritt ein Fehler auf, wenn eine neue Instanz von " [**errbemujebject**](swbemobject.md) " erstellt wird, aber für die Schlüsseleigenschaft kein Wert angegeben wird. Windows-Verwaltungsinstrumentation (WMI) generiert automatisch einen GUID-Wert (Globally Unique Identifier), aber ein GUID-Wert wird von " **errbewbject. \_ Delete**" nicht akzeptiert. In diesem Fall funktioniert " [**Swap Services. Delete**](swbemservices-delete.md)", das den Objekt Pfad verwendet. Beachten Sie, dass ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt von der Methode " [**errbemubject. Put \_**](swbemobject-put-.md) " zurückgegeben wird, nachdem ein Objekt an WMI übergeben wurde.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine neue Klasse erstellt: Fügt eine Schlüsseleigenschaft hinzu. schreibt die neue Klasse in das Repository. und zeigt den Pfad des neuen Klassen Objekts an. Das Skript erzeugt dann eine Instanz der neuen Klasse. schreibt Sie; und zeigt den Pfad an. Beachten Sie, dass das Skript sowohl die-Klasse als auch Ihre-Instanzen aus dem Repository löscht, indem einfach die-Klasse gelöscht wird.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



 

 




