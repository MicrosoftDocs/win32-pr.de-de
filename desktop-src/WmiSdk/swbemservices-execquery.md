---
description: 'SWbemServices.ExecQuery-Methode: Führt eine Abfrage aus, um Objekte abzurufen.'
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.ExecQuery-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9e827b1297a2bdd3bac39a22efa7f80e0d4723ded689e691423c6945a88bb729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897485"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.ExecQuery-Methode

Die **ExecQuery-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Abfrage aus, um Objekte abzurufen. Diese Objekte sind über die zurückgegebene [**SWbemObjectSet-Auflistung**](swbemobjectset.md) verfügbar.

Diese Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strQuery* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Text der Abfrage enthält. Dieser Parameter darf nicht leer sein. Weitere Informationen zum Erstellen von WMI-Abfragezeichenfolgen finden Sie unter Abfragen mit [WQL](querying-with-wql.md) und in der [WQL-Referenz.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält. Wenn angegeben, muss dieser Wert "WQL" sein.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten der Abfrage bestimmt und bestimmt, ob dieser Aufruf sofort zurückgegeben wird. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately.** Dieser Parameter kann die folgenden Werte akzeptieren.

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

Bewirkt, dass der Aufruf sofort zurückkehrt.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser Aufruf blockiert wird, bis die Abfrage abgeschlossen ist. Dieses Flag ruft die -Methode im synchronen Modus auf.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype** (2 (0x2))


</dt> <dd>

Wird für die Prototyperstellung verwendet. Dieses Flag verhindert, dass die Abfrage ausgeführt wird, und gibt ein Objekt zurück, das wie ein typisches Ergebnisobjekt aussieht.

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

Wenn kein Fehler auftritt, gibt diese Methode ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) zurück. Dies ist eine Objektsammlung, die das Ergebnisset der Abfrage enthält. Der Aufrufer kann die Auflistung mithilfe der Implementierung von Auflistungen für die von Ihnen verwendete Programmiersprache untersuchen. Weitere Informationen finden Sie unter [Zugreifen auf eine Auflistung.](accessing-a-collection.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecQuery-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen des Ergebnisses.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ungültiger Parameter wurde angegeben.

</dd> <dt>

**wbemErrInvalidQuery** – 2147749911 (0x80041017)
</dt> <dd>

Die Abfragesyntax ist ungültig.

</dd> <dt>

**wbemErrInvalidQueryType** – 2147749912 (0x80041018)
</dt> <dd>

Die angeforderte Abfragesprache wird nicht unterstützt.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**ExecQuery** ist einer der am häufigsten verwendeten Aufrufe zum Abrufen von WMI-Informationen. Ein Standardaufruf von **ExecQuery** sieht wie folgt aus:


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Beachten Sie, dass Sie das [**SWbemServices-Objekt**](swbemservices.md) mit einem Moniker erstellen, der den entsprechenden Namespace und die Sicherheit darstellt, und dann den **ExecQuery-Aufruf** über den Dienst ausführen. Eine vollständigere Erörterung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md) und [Aufzählen von WMI.](enumerating-wmi.md)

Wie die [**InstancesOf-Methode**](swbemservices-instancesof.md) gibt die **ExecQuery-Methode** immer eine [**SWbemObjectSet-Auflistung**](swbemobjectset.md) zurück. Daher muss Ihr WMI-Skript die Von ExecQuery zurückgegebenen Sammlungen aufzählen, um auf jede verwaltete Ressourceninstanz in der Sammlung zugreifen zu können, wie hier gezeigt:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Andere [**SWbemServices-Methoden,**](swbemservices.md) die [**ein SWbemObjectSet**](swbemobjectset.md) zurückgeben, sind [**AssociatorsOf,**](swbemservices-associatorsof.md) [**ReferencesTo**](swbemservices-referencesto.md)und [**SubclassesOf.**](swbemservices-subclassesof.md)

Es ist kein Fehler für die Abfrage, ein leeres Ergebnisset zurück zu geben. Die **ExecQuery-Methode** gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die Schlüsseleigenschaft im *strQuery-Argument angefordert* wird. Wenn beim Ausführen dieser Methode ein Fehler auftritt und Sie das **Flag wbemFlagReturnImmediately** nicht verwenden, wird das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) erst festgelegt, wenn Sie versuchen, auf den zurückgegebenen Objektsatz zu zugreifen. Wenn Sie jedoch das **Flag wbemFlagReturnWhenComplete** verwenden, wird das Err-Objekt festgelegt, wenn die **ExecQuery-Methode** aufgerufen wird.

Die Anzahl der SCHLÜSSELWÖRTER **AND** und **OR,** die in WQL-Abfragen verwendet werden können, ist begrenzt. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den **WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode** als **HRESULT-Wert** zurückgibt. Der Grenzwert für WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden alle Laufwerke auf dem lokalen Computer gefunden und die Geräte-ID und der Typ des Laufwerks angezeigt.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



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

[**SWbemServices.Get**](swbemservices-get.md)
</dt> <dt>

[Abfragen mit WQL](querying-with-wql.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> <dt>

[Aufzählen von WMI](enumerating-wmi.md)
</dt> </dl>

 

