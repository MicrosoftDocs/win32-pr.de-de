---
description: Die References- \_ Methode des-Objekts von "errbemabject" gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf das aktuelle-Objekt verweisen.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: SWbemObject.References_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868587"
---
# <a name="swbemobjectreferences_-method"></a>Errbemubject. References- \_ Methode

Die **References \_** -Methode des-Objekts von " [**errbemabject**](swbemobject.md) " gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf das aktuelle-Objekt verweisen.

Diese Methode führt dieselbe Funktion aus wie die [Verweise der](references-of-statement.md) WQL-Abfrage.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *strautclass* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*Rolle "Rolle* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftsnamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bclassesonly* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll. Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören. Der Standardwert für diesen Parameter ist **false**.

</dd> <dt>

*bschemaonly* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **false**. Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist. Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

" *stringdqualifier* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**, der den-Rückruf anweist, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird. Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Bewirkt, dass der-Rückruf sofort zurückgegeben wird.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **References \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

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

Weitere Informationen zu den verweisen der zugeordneten WQL-Abfrage, Quell Instanzen und Zuordnungs Objekte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).

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

[**"Errbemujeject. ASSOCIATORS"\_**](swbemobject-associators-.md)
</dt> <dt>

[**"Taubemservices. associatorsof"**](swbemservices-associatorsof.md)
</dt> <dt>

[**"Swap Services. referencesto"**](swbemservices-referencesto.md)
</dt> </dl>

 

 




