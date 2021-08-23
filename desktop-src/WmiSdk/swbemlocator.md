---
description: Sie können die Methoden des SWbemLocator-Objekts verwenden, um ein SWbemServices-Objekt zu erhalten, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remotehostcomputer darstellt.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: SWbemLocator-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0e93e9bd0bfb33c495b30afbde47bcb9b007acb4cd00dece42e1a8c3b88e99d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732791"
---
# <a name="swbemlocator-object"></a>SWbemLocator-Objekt

Sie können die Methoden des **SWbemLocator-Objekts** verwenden, um ein [**SWbemServices-Objekt**](swbemservices.md) zu erhalten, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remotehostcomputer darstellt. Anschließend können Sie die Methoden des **SWbemServices-Objekts** verwenden, um auf WMI zu zugreifen. Dieses Objekt kann durch den VBScript **CreateObject-Aufruf erstellt** werden.

## <a name="members"></a>Member

Das **SWbemLocator-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemLocator-Objekt** verfügt über diese Methoden.



| Methode                                              | Beschreibung                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Stellt eine Verbindung mit WMI auf dem angegebenen Computer her.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemLocator-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp          | Beschreibung                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicherheit\_**](swbemlocator-security-.md)<br/> | Schreibgeschützt<br/> | Wird zum Lesen oder Ändern der Sicherheitseinstellungen verwendet.<br/> |



 

## <a name="remarks"></a>Hinweise

Am Anfang des WMI-Skriptbibliothek-Objektmodells befindet sich das SWbemLocator-Objekt. SWbemLocator wird verwendet, um eine authentifizierte Verbindung mit einem WMI-Namespace herzustellen, ähnlich wie die VBScript GetObject-Funktion und der WMI-Moniker "winmgmts:", um eine authentifizierte Verbindung mit WMI herzustellen. SWbemLocator ist jedoch für zwei spezifische Skriptszenarien konzipiert, die nicht mit GetObject und dem WMI-Moniker ausgeführt werden können. Sie müssen SWbemLocator verwenden, wenn Sie:

-   Geben Sie Benutzer- und Kennwortanmeldeinformationen an, um eine Verbindung mit WMI auf einem Remotecomputer herzustellen. Der mit der GetObject-Funktion verwendete WMI-Moniker enthält keinen Mechanismus zum Angeben von Anmeldeinformationen. Die meisten WMI-Aktivitäten (einschließlich aller auf Remotecomputern ausgeführten) erfordern Administratorrechte. Wenn Sie sich in der Regel mit einem regulären Benutzerkonto anstelle eines Administratorkontos anmelden, können Sie die meisten WMI-Aufgaben nur ausführen, wenn Sie das Skript unter alternativen Anmeldeinformationen ausführen.
-   Verbinden WMI,wenn Sie ein WMI-Skript von einer Webseite aus ausführen. Sie können die GetObject-Funktion nicht verwenden, wenn Sie Skripts ausführen, die in eine HTML-Seite eingebettet sind, da Internet Explorer die Verwendung von GetObject aus Sicherheitsgründen nicht zugelassen.

Darüber hinaus können Sie SWbemLocator verwenden, um eine Verbindung mit WMI herzustellen, wenn Die mit GetObject verwendete WMI-Verbindungszeichenfolge verwirrend oder schwierig ist.

Sie verwenden CreateObject anstelle von GetObject, um einen Verweis auf SWbemLocator zu erstellen. Um den Verweis zu erstellen, müssen Sie der CreateObject-Funktion den programmgesteuerten SWbemLocator-Bezeichner (ProgID) "WbemScripting.SWbemLocator" übergeben, wie in Zeile 2 im folgenden Skriptbeispiel gezeigt. Nachdem Sie einen Verweis auf ein SWbemLocator-Objekt erhalten haben, rufen Sie die ConnectServer-Methode auf, um eine Verbindung mit WMI herzustellen und einen Verweis auf ein SWbemServices-Objekt zu erhalten. Dies wird in Zeile 3 des folgenden Skripts gezeigt.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Um ein Skript unter alternativen Anmeldeinformationen auszuführen, fügen Sie den Benutzernamen und das Kennwort als zusätzliche Parameter ein, die an ConnectServer übergeben werden. Dieses Skript wird beispielsweise mit den Anmeldeinformationen eines Benutzers namens kenmyer mit dem Kennwort homerj ausgeführt.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Sie können auch das Format \\ Domänenbenutzername verwenden, um einen Benutzernamen anzugeben. Beispiel:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Beispiel wird **SWbemLocator verwendet,** um eine Verbindung mit einem Server herzustellen.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




