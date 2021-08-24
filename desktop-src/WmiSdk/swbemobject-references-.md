---
description: Die \_ References-Methode des SWbemObject-Objekts gibt eine Auflistung aller Zuordnungsklassen oder Instanzen zurück, die auf das aktuelle Objekt verweisen.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: SWbemObject.References_-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 527d49854f57937cfbcff8fd033381472f81cb15dc7ec1f4122a185fff33aa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860210"
---
# <a name="swbemobjectreferences_-method"></a>SWbemObject.References-Methode \_

Die **\_ References-Methode** des [**SWbemObject-Objekts**](swbemobject.md) gibt eine Auflistung aller Zuordnungsklassen oder Instanzen zurück, die auf das aktuelle Objekt verweisen.

Diese Methode führt die gleiche Funktion wie die [REFERENCES OF](references-of-statement.md) WQL-Abfrage aus.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

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

*strResultClass* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*strRole* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Eigenschaftennamen enthält. Falls angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte auf die Objekte beschränkt werden müssen, in denen das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bClassesOnly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle von tatsächlichen Instanzen der Klassen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Zuordnungsobjekte gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE** festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist. Bei Festlegung auf **TRUE** stellt der Satz zurückgegebener Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

*strRequiredQualifier* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte den angegebenen Qualifizierer enthalten müssen.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately,** der den Aufruf anleitet, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly** (32 (0x20))


</dt> <dd>

Bewirkt, dass ein vorwärts gerichteter Enumerator zurückgegeben wird. Vorwärts-Enumeratoren sind im Allgemeinen viel schneller und verwenden weniger Arbeitsspeicher als herkömmliche Enumeratoren, lassen jedoch keine Aufrufe von [**SWbemObject.Clone \_**](swbemobject-clone-.md)zu.

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional** (0 (0x0))


</dt> <dd>

Bewirkt, dass Windows Management Instrumentation (WMI) Zeiger auf Objekte der Enumeration beibehält, bis der Client den Enumerator freigibt.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Bewirkt, dass der Aufruf sofort zurückgegeben wird.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete( (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser Aufruf blockiert wird, bis die Abfrage abgeschlossen ist.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers( (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurückgibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Aufruf erfolgreich ist, wird ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ References-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung, eine oder mehrere der vom Aufruf zurückgegebenen Klassen anzuzeigen.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zu den REFERENCES OF zugeordneten WQL-Abfragen, Quellinstanzen und Zuordnungsobjekten finden Sie unter [ASSOCIATORS OF-Anweisung.](associators-of-statement.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




