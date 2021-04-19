---
description: Die subclasses- \_ Methode des "errbemubject"-Objekts gibt ein "errbewbjectset"-Objekt zurück.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: SWbemObject.Subclasses_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348284"
---
# <a name="swbemobjectsubclasses_-method"></a>Methode "errbemubject. subclasses" \_

Die **subclasses \_** -Methode des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück. Dieses Objekt ist eine Auflistung von Unterklassen des aktuellen-Objekts, das eine-Klasse sein muss. Elemente in der zurückgegebenen Auflistung können mithilfe von Standard Auflistungs Methoden abgerufen werden. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die bestimmt, wie detailliert der aufzurufende Aufzählung Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep * * * * (0 (0x0))


</dt> <dd>

Erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden. Die übergeordnete Klasse selbst wird nicht in der-Enumeration zurückgegeben.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache * * * * (1 (0x1))


</dt> <dd>

Standardwert für diesen Parameter. Es erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Bewirkt, dass der-Rückruf sofort zurückgegeben wird

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser-Vorgang blockiert wird, bis der-Befehl abgeschlossen ist.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Unterklassen \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es ist kein Fehler, wenn die zurückgegebene Auflistung keine Elemente enthält, wenn keine Unterklassen des aktuellen-Objekts vorhanden sind. Die **Unterklassen \_** Methode funktioniert nur für Klassen Objekte.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> <dt>

[**Austauschen von "errbemubjectset"**](swbemobjectset.md)
</dt> </dl>

 

 




