---
description: Gibt eine Auflistung aller Zuordnungsklassen oder -instanzen zurück, die auf eine bestimmte Quellklasse oder Instanz verweisen.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: SWbemServices.ReferencesTo-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b703ab1384286ecfc3a797f88ec18cafe8b6142acf586c7f96e4ae9b4085f7cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312499"
---
# <a name="swbemservicesreferencesto-method"></a>SWbemServices.ReferencesTo-Methode

Die **ReferencesTo-Methode** des [**SWbemServices-Objekts**](swbemservices.md) gibt eine Auflistung aller Zuordnungsklassen oder -instanzen zurück, die auf eine bestimmte Quellklasse oder -instanz verweisen. Diese Methode führt die gleiche Funktion wie die [REFERENCES OF](references-of-statement.md) WQL-Abfrage aus.

Diese Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Zeichenfolge, die den Objektpfad der Quelle für diese Methode enthält. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strResultClass* \[ Optional\]
</dt> <dd>

Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*strRole* \[ Optional\]
</dt> <dd>

Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte auf die Objekte beschränkt werden müssen, in denen das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bClassesOnly* \[ Optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle von tatsächlichen Instanzen der Klassen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Zuordnungsobjekte gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE** festgelegt werden, wenn der *strObjectPath-Parameter* den Objektpfad einer Klasse angibt. Bei Festlegung auf **TRUE** stellt der Satz zurückgegebener Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

*strRequiredQualifier* \[ Optional\]
</dt> <dd>

Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte den angegebenen Qualifizierer enthalten müssen.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately,** der den Aufruf anleitet, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly( (32 (0x20))


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

Bewirkt, dass dieser Aufruf blockiert wird, bis die Abfrage abgeschlossen ist. Dieses Flag ruft die -Methode im synchronen Modus auf.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers( (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten zusammen mit der Basisklassendefinition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt die Methode ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ReferencesTo-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

> [!Note]  
> Eine zurückgegebene Auflistung mit null Elementen ist kein Fehler.

 

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

</dd> <dt>

**wbemFlagUseAmendedQualifiers** – 131072 (0x20000)
</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurückgibt.

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
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




