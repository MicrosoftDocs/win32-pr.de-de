---
description: Die \_ Put-Methode von SWbemObject erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows Management Instrumentation (WMI). Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem SWbemObject geändert haben und Ihre Änderungen in WMI geschrieben wurden.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9310f690ea9ffc153e88ee9b0cd5ed489beef107c048f7e00e6891a69800b957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991970"
---
# <a name="swbemobjectput_-method"></a>SWbemObject.Put-Methode \_

Die **\_ Put-Methode** von [**SWbemObject**](swbemobject.md) erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows Management Instrumentation (WMI). Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem **SWbemObject** geändert haben und Ihre Änderungen in WMI geschrieben wurden.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Dieser Parameter bestimmt, ob der Aufruf die Klasse oder Instanz erstellt oder aktualisiert und ob der Aufruf sofort zurückgegeben wird. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible( 0 (0x0))


</dt> <dd>

Ermöglicht das Aktualisieren einer Klasse, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind. Sie ermöglicht auch Updates in allen Fällen, wenn die Änderung nur  an unwichtige Qualifizierer (z. B. den Description-Qualifizierer) erfolgt. Dies ist das Standardverhalten für diesen Aufruf und wird für die Kompatibilität mit früheren Versionen von WMI verwendet. Wenn die -Klasse Über -Instanzen verfügt, schlägt das Update fehl.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode( (32 (0x20))


</dt> <dd>

Ermöglicht Updates von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Sie können dieses Flag verwenden, wenn Sie einer Basisklasse, die zuvor in keiner der untergeordneten Klassen erwähnt wurde, eine neue Eigenschaft hinzufügen. Wenn die -Klasse Über -Instanzen verfügt, schlägt das Update fehl. Wenn die -Klasse Über -Instanzen verfügt, schlägt das Update fehl.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode( (64 (0x40))


</dt> <dd>

Dieses Flag erzwingt Aktualisierungen von Klassen, wenn in Konflikt stehende untergeordnete Klassen vorhanden sind. Mit diesem Flag wird z. B. ein Update erzwingen, wenn ein Klassenqualifizierer in einer untergeordneten Klasse definiert wurde und die Basisklasse versucht, den gleichen Qualifizierer hinzuzufügen, der mit dem vorhandenen in Konflikt steht. Im Force-Modus würde dieser Konflikt gelöst werden, indem der in Konflikt stehende Qualifizierer in der untergeordneten Klasse gelöscht wird. Wenn die Klasse über Instanzen verfügt, schlägt das Update fehl.

Die Verwendung des Force-Modus zum Aktualisieren einer statischen Klasse führt zum Löschen aller Instanzen dieser Klasse. Bei einem erzwungenen Update für eine Anbieterklasse werden keine Instanzen der -Klasse gelöscht.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate** (0 (0x0))


</dt> <dd>

Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn sie nicht vorhanden ist, oder überschrieben wird, wenn sie bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly** (2 (0x2))


</dt> <dd>

Wird nur für die Erstellung verwendet. Der Aufruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly( 1 (0x1))


</dt> <dd>

Bewirkt, dass dieser Aufruf aktualisiert wird. Die Klasse oder Instanz muss vorhanden sein, damit der Aufruf erfolgreich ist.

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

Bewirkt, dass WMI Klassenänderungsdaten sowie die Basisklassendefinition schreibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemObjectPath-Objekt,**](swbemobjectpath.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Aufruf erfolgreich ist, wird ein [**SWbemObjectPath-Objekt**](swbemobjectpath.md) zurückgegeben. Dieses Objekt enthält den Objektpfad der Instanz oder Klasse, für die erfolgreich ein Commit für WMI ausgeführt wurde.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ Put-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Aktualisieren einer Instanz der angegebenen Klasse.

</dd> <dt>

**wbemErrAlreadyExists** – 2147749913 (0x80041019)
</dt> <dd>

Das **Flag wbemChangeFlagCreateOnly** wurde angegeben, aber die Instanz ist bereits vorhanden.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrBiogalNull** – 2147749898 (0x8004100A)
</dt> <dd>

Für eine Eigenschaft, die möglicherweise nicht **Nothing** ist, wurde der Wert **Nothing** angegeben. Ein Beispiel für eine solche Eigenschaft ist eine , die durch einen **Key-,** **Indexed-** oder **Not \_ NULL-Qualifizierer** gekennzeichnet ist.

</dd> <dt>

**wbemErrInvalidObject** – 2147749908 (0x80041014)
</dt> <dd>

Die angegebene Instanz ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** – 0x80041008
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das **Flag wbemChangeFlagUpdateOnly** wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

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

[**SWbemObjectPath.Class**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

