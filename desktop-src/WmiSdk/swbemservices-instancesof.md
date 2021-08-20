---
description: Erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: SWbemServices.InstancesOf-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 9c53b3f27b570f2fab76cb2164c4a029ad21cfccfe7bff52f2c5b9d8d55bf9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107963"
---
# <a name="swbemservicesinstancesof-method"></a>SWbemServices.InstancesOf-Methode

Die **InstancesOf-Methode** des [**SWbemServices-Objekts**](swbemservices.md) erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt. Diese Methode implementiert eine einfache Abfrage. Komplexere Abfragen erfordern möglicherweise die Verwendung vonSWbemServices.Exe [**cQuery.**](swbemservices-execquery.md)

Die -Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

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

*strClass* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Namen der Klasse enthält, für die Instanzen gewünscht werden. Dieser Parameter darf nicht leer sein.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Dieser Parameter bestimmt, wie detailliert der Aufruf aufzählt und ob dieser Aufruf sofort zurückgegeben wird. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately.** Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly( (32 (0x20))


</dt> <dd>

Bewirkt, dass ein vorwärts enumerator zurückgegeben wird. Vorwärts-Enumeratoren sind im Allgemeinen viel schneller und verwenden weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber sie lassen keine Aufrufe von [**SWbemObject.Clone zu. \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional** (0 (0x0))


</dt> <dd>

Bewirkt, dass WMI Zeiger auf Objekte der Enumeration beibehalten, bis der Client den Enumerator frei gibt.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately( (16 (0x10))


</dt> <dd>

Standardwert für diesen Parameter. Dieses Flag bewirkt, dass der Aufruf sofort zurückkehrt.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser Aufruf blockiert wird, bis die Abfrage abgeschlossen ist. Dieses Flag ruft die -Methode im synchronen Modus auf.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow** (1 (0x1))


</dt> <dd>

Erzwingt, dass die -Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse enthält.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep** (0 (0x0))


</dt> <dd>

Standardwert für diesen Parameter. Dieser Wert erzwingt, dass die -Enumeration alle Klassen in der Hierarchie enthält.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurück gibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt die Methode ein [**SWbemObjectSet zurück.**](swbemobjectset.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **InstancesOf-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

> [!Note]  
> Ein zurückgegebener Enumerator mit null Elementen ist kein Fehler.

 

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Nicht angegebener Fehler.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **InstancesOf-Methode** funktioniert nur für Klassenobjekte.

Standardmäßig führt InstancesOf einen tiefen Abruf durch. Das heißt, InstancesOf ruft alle Instanzen der verwalteten Ressource ab, die Sie identifizieren, und alle Instanzen aller Unterklassen, die unter der Zielklasse definiert sind. Das folgende Skript ruft beispielsweise alle Ressourcen ab, die von allen dynamischen Klassen modelliert werden, die unter der abstrakten \_ CIM-Dienstklasse definiert sind.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



Wenn Sie dieses Skript ausführen, erhalten Sie Informationen zurück. Diese Informationen sind jedoch nicht auf die dienste beschränkt, die auf einem Computer installiert sind. Stattdessen enthält sie Informationen aus allen untergeordneten Klassen des CIM-Diensts, einschließlich [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) und [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)). [**\_**](/windows/desktop/CIMWin32Prov/cim-service)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

