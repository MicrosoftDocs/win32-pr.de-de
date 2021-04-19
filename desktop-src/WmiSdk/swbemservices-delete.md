---
description: Löscht die im Objekt Pfad angegebene Klasse oder Instanz. Sie können nur Objekte im aktuellen Namespace löschen.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Methode ' Swap Services. delete ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485443"
---
# <a name="swbemservicesdelete-method"></a>Swap Services. Delete-Methode

Die **Delete** -Methode des [**Swap Services**](swbemservices.md) -Objekts löscht die im Objekt Pfad angegebene Klasse oder Instanz. Sie können nur Objekte im aktuellen Namespace löschen.

Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, können Sie dieses Objekt nur dann löschen, wenn der Anbieter das Löschen von Klassen oder Instanzen unterstützt.

Diese Methode wird im synchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strobjectpath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objekt Pfad zu dem Objekt enthält, das Sie löschen möchten. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Reserviert. Dieser Wert muss null (0) sein.

</dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Delete** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

Die Methode " **waybemservices. Delete** " kann verwendet werden, wenn der Schlüsseleigenschaft für das Objekt kein Wert zugewiesen wird, da diese Methode nur einen Objekt Pfad als Eingabe erfordert. Diese Methode kann in Situationen verwendet werden, in denen das Austauschen von " [**errbemubject. Delete \_**](swbemobject-delete-.md) " aufgrund eines fehlenden Schlüssel Werts fehlschlägt. Wenn das Objekt über die Datei " [**Swap. Put \_**](swbemobject-put-.md)" in WMI übernommen wird, wurde ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt durch den-Befehl abgerufen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine neue Klasse erstellt, eine Eigenschaft hinzugefügt, die kein Schlüssel ist, die neue Klasse in das Repository schreibt, und der Pfad des neuen Klassen Objekts wird angezeigt. Das Skript erzeugt dann eine Instanz der neuen Klasse, schreibt die Instanz und zeigt den Pfad an. Beachten Sie, dass das Skript sowohl die-Klasse als auch Ihre-Instanzen aus dem Repository löscht, indem die-Klasse gelöscht wird. Weitere Informationen zu WMI-Klassen und-Instanzen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und [Common Information Model](common-information-model.md).


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
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
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**Errbemubjectpath**](swbemobjectpath.md)
</dt> </dl>

 

 




