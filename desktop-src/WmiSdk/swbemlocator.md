---
description: Mit den Methoden des-Objekts von "Swap-Locator" können Sie ein-Objekt abrufen, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remote Host Computer darstellt.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Swap-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348660"
---
# <a name="swbemlocator-object"></a>Swap-Objekt

Mit den Methoden des-Objekts von " **Swap-Locator** " können Sie [**ein-**](swbemservices.md) Objekt abrufen, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remote Host Computer darstellt. Anschließend können Sie die Methoden des WS- **Services** -Objekts verwenden, um auf WMI zuzugreifen. Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **Swap-Locator** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemlocator** -Objekt verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**Server Verbindung**](swbemlocator-connectserver.md) | Stellt eine Verbindung mit WMI auf dem angegebenen Computer her.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **taubemlocator** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp          | BESCHREIBUNG                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicherheit\_**](swbemlocator-security-.md)<br/> | Schreibgeschützt<br/> | Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Am Anfang des WMI-skriptingbibliotheks-Objektmodells befindet sich das Objekt "Swap-Locator". Mithilfe von "Swap-Locator" wird eine authentifizierte Verbindung mit einem WMI-Namespace hergestellt, ähnlich wie die VBScript-Funktion "GetObject" und der WMI-Moniker "winmgmts:" zum Herstellen einer authentifizierten Verbindung mit WMI. Allerdings ist der Austausch Vorgang so konzipiert, dass zwei spezifische Skript Szenarien adressiert werden, die nicht mithilfe von GetObject und dem WMI-Moniker ausgeführt werden können. Wenn Sie Folgendes benötigen, müssen Sie den folgenden Befehl verwenden:

-   Geben Sie Benutzer-und Kenn Wort Anmelde Informationen für die Verbindung mit WMI auf einem Remote Computer an. Der WMI-Moniker, der mit der GetObject-Funktion verwendet wird, enthält keinen Mechanismus zum Angeben von Anmelde Informationen. Die meisten WMI-Aktivitäten (einschließlich aller auf Remote Computern ausgeführten) erfordern Administratorrechte. Wenn Sie sich in der Regel mit einem regulären Benutzerkonto anstelle eines Administrator Kontos anmelden, können Sie die meisten WMI-Aufgaben nur ausführen, wenn Sie das Skript unter Alternative Anmelde Informationen ausführen.
-   Stellen Sie eine Verbindung mit WMI her, wenn Sie ein WMI-Skript aus einer Webseite heraus ausführen. Sie können die GetObject-Funktion nicht verwenden, wenn Sie Skripts ausführen, die in einer HTML-Seite eingebettet sind, da Internet Explorer die Verwendung von GetObject aus Sicherheitsgründen nicht zulässt.

Außerdem empfiehlt es sich, für die Verbindung mit WMI die Verbindung mit WMI zu verwenden, wenn Sie die WMI-Verbindungs Zeichenfolge mit "GetObject" verwirrend oder schwierig finden.

Sie verwenden "" anstelle von "GetObject", um einen Verweis auf "Swap" zu erstellen. Um den Verweis zu erstellen, müssen Sie die Funktion "degid" ("WbemScripting. Swap") der Funktion "degid" ("WbemScripting. sexbemlocator") der Funktion "degid" übergeben, wie in Zeile 2 im folgenden Skript Beispiel gezeigt. Nachdem Sie einen Verweis auf ein Objekt vom Typ "WS-Locator" abgerufen haben, rufen Sie die ConnectServer-Methode auf, um eine Verbindung mit WMI herzustellen und einen Verweis auf ein Objekt vom Typ "WS Dies wird in Zeile 3 des folgenden Skripts veranschaulicht.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Wenn Sie ein Skript unter Alternativen Anmelde Informationen ausführen möchten, fügen Sie den Benutzernamen und das Kennwort als zusätzliche Parameter an ConnectServer ein. Dieses Skript wird z. b. unter den Anmelde Informationen eines Benutzers namens kenmyer mit dem Kennwort homerj ausgeführt.


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



Sie können auch das Format Domäne \\ Benutzername verwenden, um einen Benutzernamen anzugeben. Beispiel:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Beispiel wird **SWbemLocator** verwendet, um eine Verbindung mit einem Server herzustellen.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch<br/>                                                          |
| IID<br/>                      | IID \_ iswbemlocator<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




