---
description: Die Put- \_ Methode von "errbemubject" erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI). Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem Swap-Objekt geändert haben, und Ihre Änderungen werden in WMI geschrieben.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347065"
---
# <a name="swbemobjectput_-method"></a>Errbemubject. Put- \_ Methode

Die **Put \_** -Methode von " [**errbemubject**](swbemobject.md) " erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI). Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem **Swap-Objekt** geändert haben, und Ihre Änderungen werden in WMI geschrieben.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Dieser Parameter bestimmt, ob der-Befehl die Klasse oder Instanz erstellt oder aktualisiert und ob der Rückruf sofort zurückgegeben wird. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemchangeflagupdatecompatible * * * * (0 (0x0))


</dt> <dd>

Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind. Es lässt auch Updates in allen Fällen zu, wenn die Änderung lediglich an unbedeutende Qualifizierer (z. b. der **Beschreibungs** Qualifizierer) erfolgt. Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet. Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemchangeflagupdatesafemode * * * * (32 (0x20))


</dt> <dd>

Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Sie können dieses Flag verwenden, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor nicht in einer der untergeordneten Klassen erwähnt wurde. Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl. Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Wbemchangeflagupdateforcemode * * * * (64 (0x40))


</dt> <dd>

Dieses Flag erzwingt die Aktualisierung von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind. Dieses Flag erzwingt z. b. eine Aktualisierung, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert wurde, und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen und in Konflikt mit dem vorhandenen zu suchen. Im Force-Modus würde dieser Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse behoben werden. Wenn die Klasse über Instanzen verfügt, kann das Update nicht ausgeführt werden.

Wenn Sie eine statische Klasse mithilfe des Force-Modus aktualisieren, werden alle Instanzen dieser Klasse gelöscht. Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemchangeflagkreateorupdate * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist oder überschrieben wird, wenn Sie bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemchangeflagkreateonly * * * * (2 (0x2))


</dt> <dd>

Wird nur für die Erstellung verwendet. Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemchangeflagupdateonly * * * * (1 (0x1))


</dt> <dd>

Bewirkt, dass dieser Update Vorgang aktualisiert wird. Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.

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

Bewirkt, dass WMI Klassen Zusatzdaten und die Basisklassen Definition schreibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich um ein Objekt vom Typ" [**errbemujectpath**](swbemobjectpath.md) ", dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurückgegeben. Dieses Objekt enthält den Objekt Pfad der-Instanz oder der-Klasse, für die erfolgreich ein Commit in WMI durchgeführt wurde.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Put \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Aktualisieren einer Instanz der angegebenen Klasse.

</dd> <dt>

**wbemErrAlreadyExists** -2147749913 (0x80041019)
</dt> <dd>

Das Flag " **wbemchangeflagkreateonly** " wurde angegeben, aber die Instanz ist bereits vorhanden.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrIllegalNull** -2147749898 (0x8004100a)
</dt> <dd>

Der Wert **Nothing** wurde für eine Eigenschaft angegeben, die möglicherweise nicht " **Nothing**" ist. Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen **Schlüssel-,** **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

Die angegebene Instanz ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** -0x80041008
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das Flag " **wbemchangeflagupdateonly** " wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

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

[**Errbemubjectpath. Class**](swbemobjectpath-class.md)
</dt> <dt>

[**Swap Property**](swbemproperty.md)
</dt> <dt>

[**Austausch Qualifizierer**](swbemqualifier.md)
</dt> </dl>

 

