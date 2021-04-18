---
description: Führt eine Abfrage zum Abrufen von Objekten aus.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Execquery-Methode (wbemdisp. h)
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
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359099"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Execquery-Methode

Die **ExecQuery** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Abfrage zum Abrufen von-Objekten aus. Diese Objekte sind über die zurückgegebene [**errbewbjectset**](swbemobjectset.md) -Auflistung verfügbar.

Diese Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*"-Abfrage"* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Text der Abfrage enthält. Dieser Parameter darf nicht leer sein. Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.

</dd> <dt>

"in der *Sprache* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält. Wenn angegeben, muss dieser Wert "WQL" lauten.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten der Abfrage bestimmt und bestimmt, ob dieser Rückruf sofort zurückgegeben wird. Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**. Dieser Parameter kann die folgenden Werte annehmen.

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

Bewirkt, dass der-Rückruf sofort zurückgegeben wird.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass dieser-Vorgang blockiert wird, bis die Abfrage beendet ist. Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemqueryflagprototype * * * * (2 (0x2))


</dt> <dd>

Wird zum Prototypen verwendet. Dieses Flag verhindert, dass die Abfrage ausgeführt wird, und gibt ein Objekt zurück, das wie ein typisches Ergebnis Objekt aussieht.

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

Wenn kein Fehler auftritt, gibt diese Methode ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück. Dies ist eine Objekt Auflistung, die das Resultset der Abfrage enthält. Der Aufrufer kann die Auflistung mithilfe der Implementierung von Auflistungen für die verwendete Programmiersprache untersuchen. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecQuery** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen des Resultsets.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Die Abfrage Syntax ist ungültig.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Die angeforderte Abfragesprache wird nicht unterstützt.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**ExecQuery** ist einer der am häufigsten verwendeten Aufrufe zum Abrufen von WMI-Informationen. Ein standardmäßiger Befehl von **ExecQuery** sieht wie folgt aus:


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



Beachten Sie, dass Sie das Objekt " [**bulbemservices**](swbemservices.md) " mit einem Moniker erstellen, der den entsprechenden Namespace und die Sicherheit darstellt, und dann den **ExecQuery** -Aufruf über den Dienst durchführen. Eine ausführlichere Erläuterung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md) und [Aufzählen von WMI](enumerating-wmi.md).

Wie die [**InstancesOf**](swbemservices-instancesof.md) -Methode gibt die **ExecQuery** -Methode immer eine [**errbewbjectset**](swbemobjectset.md) -Auflistung zurück. Daher muss das WMI-Skript die Auflistung von ExecQuery-Rückgaben auflisten, um auf jede verwaltete Ressourcen Instanz in der Auflistung zuzugreifen, wie hier gezeigt:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Andere " [**errbemservices**](swbemservices.md) "-Methoden, die ein " [**errbewbjectset**](swbemobjectset.md) " zurückgeben, umfassen [**associatorsof**](swbemservices-associatorsof.md), [**referencesto**](swbemservices-referencesto.md)und [**SubclassesOf**](swbemservices-subclassesof.md).

Es ist kein Fehler, wenn die Abfrage ein leeres Resultset zurückgibt. Die **ExecQuery** -Methode gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die Key-Eigenschaft im " *strinquery* "-Argument angefordert wurde. Wenn beim Ausführen dieser Methode ein Fehler auftritt und Sie das **wbemFlagReturnImmediately** -Flag nicht verwenden, wird das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt erst festgelegt, wenn Sie versuchen, auf den zurückgegebenen Objekt Satz zuzugreifen. Wenn Sie jedoch das **wbemflagreturnjecomplete** -Flag verwenden, wird das Err-Objekt festgelegt, wenn die **ExecQuery** -Methode aufgerufen wird.

Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den Fehlercode für die **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt. Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden alle Laufwerke auf dem lokalen Computer und die Geräte-ID und der Typ des Laufwerks angezeigt.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**Austauschdienste. Get**](swbemservices-get.md)
</dt> <dt>

[Abfragen mit WQL](querying-with-wql.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> <dt>

[Auflisten von WMI](enumerating-wmi.md)
</dt> </dl>

 

