---
description: Gibt ein "errbemubjectpath"-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Methode ' Swap servicesex. Put ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357464"
---
# <a name="swbemservicesexput-method"></a>Methode ' Swap servicesex. Put '

Die **Put** -Methode des Objekts " [**errbemservicesex**](swbemservicesex.md) " speichert das Objekt in dem Namespace, der an das-Objekt gebunden ist, und gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.

Diese Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemujekt* 
</dt> <dd>

Erforderlich. Das neue-Objekt, das in den-Namespace eingefügt werden soll. Dabei kann es sich um ein neu erstelltes Objekt oder um ein geändertes Objekt handeln.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Dieser Parameter bestimmt, ob der-Befehl das-Objekt erstellt oder aktualisiert und ob der-Rückruf sofort zurückgegeben wird. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemchangeflagupdatecompatible** (0 (0x0))


</dt> <dd>

Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind. Sie ermöglicht auch Updates in allen Fällen, wenn die Änderung nur an wichtigen Qualifizierern (z. b. der **Beschreibungs** Qualifizierer) vorgenommen wird. Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet. Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemchangeflagupdatesafemode** (32 (0x20))


</dt> <dd>

Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Sie können dieses Flag verwenden, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor nicht in einer der untergeordneten Klassen erwähnt wurde. Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemchangeflagupdateforcemode** (64 (0x40))


</dt> <dd>

Dieses Flag erzwingt die Aktualisierung von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind. Beispielsweise erzwingt dieses Flag ein Update, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert wurde, und die Basisklasse versucht, denselben Qualifizierer in Konflikt mit dem vorhandenen zu addieren. Im Force-Modus wird dieser Konflikt gelöst, indem der widersprüchliche Qualifizierer in der untergeordneten Klasse gelöscht wird. Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.

Die Verwendung des Force-Modus zum Aktualisieren einer statischen Klasse bewirkt, dass alle Instanzen dieser Klasse gelöscht werden. Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemchangeflagkreateorupdate** (0 (0x0))


</dt> <dd>

Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist, oder überschrieben, wenn Sie bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemchangeflagkreateonly** (2 (0x2))


</dt> <dd>

Wird nur für die Erstellung verwendet. Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemchangeflagupdateonly** (1 (0x1))


</dt> <dd>

Bewirkt, dass dieser-Befehl nur ein Update durchführen kann. Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Bewirkt, dass der-Rückruf sofort zurückgegeben wird.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemflagreturn. Complete** (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser-Vorgang blockiert wird, bis der Vorgang abgeschlossen ist. Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemflaguseamendedqualifizierer** (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassen Zusatzdaten und die Basisklassen Definition schreibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurückgegeben. Dieses Objekt enthält den Objekt Pfad der-Instanz oder der-Klasse, für die erfolgreich ein Commit in WMI durchgeführt wurde.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Put** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Vorgang.

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

Für eine Eigenschaft, die nicht **null** sein darf, wurde ein **null** -Wert angegeben. Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen [**Schlüssel**](standard-qualifiers.md)-, **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

Das angegebene Objekt ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
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
| CLSID<br/>                    | CLSID \_ iswbemservicesex<br/>                                                      |
| IID<br/>                      | IID \_ iswbemservicesex<br/>                                                        |



 

 




