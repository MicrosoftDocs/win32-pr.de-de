---
description: Erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: "' Swap Services. InstancesOf '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868571"
---
# <a name="swbemservicesinstancesof-method"></a>Swap Services. InstancesOf-Methode

Die **InstancesOf** -Methode des [**Swap Services**](swbemservices.md) -Objekts erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt. Diese Methode implementiert eine einfache Abfrage. Komplexere Abfragen erfordern möglicherweise die Verwendung von [**SWbemServices.Execquery**](swbemservices-execquery.md).

Die-Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Klasse* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Namen der Klasse enthält, für die-Instanzen gewünscht werden. Dieser Parameter darf nicht leer sein.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Dieser Parameter bestimmt, wie detailliert der aufzurufende Aufzählung und ob dieser aufgerufen wird, sobald dieser aufgerufen wird. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird. Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Standardwert für diesen Parameter. Dieses Flag bewirkt, dass der-Rückruf sofort zurückgegeben wird.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist. Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache * * * * (1 (0x1))


</dt> <dd>

Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep * * * * (0 (0x0))


</dt> <dd>

Standardwert für diesen Parameter. Dieser Wert erzwingt, dass die Enumeration alle Klassen in der Hierarchie einschließt.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt die Methode einen " [**errbewbjectset**](swbemobjectset.md)" zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **InstancesOf** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

> [!Note]  
> Ein zurückgegebener Enumerator mit 0 (null) Elementen ist kein Fehler.

 

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Nicht angegebener Fehler.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **InstancesOf** -Methode funktioniert nur für Klassen Objekte.

Standardmäßig führt InstancesOf einen Deep-Abruf durch. Das heißt, dass InstancesOf alle Instanzen der verwalteten Ressource, die Sie identifizieren, und alle Instanzen aller Unterklassen, die unter der Zielklasse definiert sind, abruft. Das folgende Skript ruft z. b. alle Ressourcen ab, die von allen dynamischen Klassen modelliert werden, die unter der \_ abstrakten Klasse des CIM-Dienstanbieter definiert sind.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



Wenn Sie dieses Skript ausführen, erhalten Sie Informationen zurück. Diese Informationen werden jedoch nicht auf die auf einem Computer installierten Dienste beschränkt. Stattdessen enthält Sie Informationen von allen untergeordneten Klassen des [**CIM- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/cim-service), einschließlich [**Win32 \_ System Driver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) und [**Win32 \_ applicationservice**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).

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

[**Austauschen von "errbemubjectset"**](swbemobjectset.md)
</dt> </dl>

 

