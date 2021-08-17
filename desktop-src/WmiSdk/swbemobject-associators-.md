---
description: Die \_ Associators-Methode des SWbemObject-Objekts gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die dem aktuellen Objekt zugeordnet sind.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: SWbemObject.Associators_-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 87458cec77a6b003a6dd35d0fc0f1a39fb785522401b46fa50a515f869760889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857430"
---
# <a name="swbemobjectassociators_-method"></a>SWbemObject.Associators-Methode \_

Die **Associators-Methode \_** des [**SWbemObject-Objekts**](swbemobject.md) gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die dem aktuellen Objekt zugeordnet sind. Diese zurückgegebenen Objekte werden endpunkte genannt. Diese Methode führt die gleiche Funktion wie die ASSOCIATORS OF WQL-Abfrage aus.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strAssocClass* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die eine Zuordnungsklasse enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der Quelle über die angegebene Zuordnungsklasse oder eine von dieser Zuordnungsklasse abgeleitete Klasse zugeordnet werden müssen.

</dd> <dt>

*strResultClass* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*strResultRole* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quellobjekt spielen müssen. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*strRole* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quellobjekt teilnehmen müssen, in dem das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bClassesOnly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle von tatsächlichen Instanzen der Klassen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Endpunktinstanzen gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, optional\]
</dt> <dd>

Dies ist ein boolescher Wert, der angibt, ob die Abfrage für das Schema und nicht für die Daten gilt. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE** festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist. Bei Festlegung auf **TRUE** stellen die zurückgegebenen Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

*strRequiredAssocQualifier* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Qualifizierernamen enthält. Dieser Parameter gibt, sofern angegeben, an, dass die zurückgegebenen Endpunkte dem Quellobjekt über eine Zuordnungsklasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält.

</dd> <dt>

*strRequiredQualifier* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die einen Qualifizierernamen enthält. Dieser Parameter gibt, sofern angegeben, an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer enthalten müssen.

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

Bewirkt, dass WMI Zeiger auf Objekte der Enumeration beibehält, bis der Client den Enumerator freigibt.

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

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurückgibt. Durch Das Einschließen dieses Flags wird der lokalisierte Beschreibungsqualifizierertext für Klassen, Eigenschaften und Methoden verfügbar. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Aufruf erfolgreich ist, wird ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Associators-Methode \_** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

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

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zur ASSOCIATORS OF zugeordneten WQL-Abfrage, Quellinstanzen und Endpunkte finden Sie unter [ASSOCIATORS OF-Anweisung.](associators-of-statement.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




