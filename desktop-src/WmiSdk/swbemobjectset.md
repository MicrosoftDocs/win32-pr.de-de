---
description: Ein SWbemObjectSet-Objekt ist eine Auflistung von SWbemObject-Objekten. Weitere Informationen finden Sie unter Zugreifen auf eine Sammlung. Dieses Objekt kann nicht durch den VBScript-CreateObject-Aufruf erstellt werden.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: SWbemObjectSet-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 33cefd39dc0e860906bc99b1f591a87dae845d6a9317410ce4850fb1a54ea708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857100"
---
# <a name="swbemobjectset-object"></a>SWbemObjectSet-Objekt

Ein **SWbemObjectSet-Objekt** ist eine Auflistung von [**SWbemObject-Objekten.**](swbemobject.md) Weitere Informationen finden Sie unter [Zugreifen auf eine Sammlung.](accessing-a-collection.md) Dieses Objekt kann nicht durch den **VBScript-CreateObject-Aufruf** erstellt werden.

Sie können ein **SWbemObjectSet-Objekt** abrufen, indem Sie eine der folgenden Methoden oder deren asynchrone Entsprechungen aufrufen:

-   [**SWbemObject.Associators\_**](swbemobject-associators-.md)
-   [**SWbemObject.Instances\_**](swbemobject-instances-.md)
-   [**SWbemObject.References\_**](swbemobject-references-.md)
-   [**SWbemObject.Subclasses\_**](swbemobject-subclasses-.md)
-   [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> Das **SWbemObjectSet-Objekt** unterstützt die optionalen **Add-** und **Remove-Auflistungsmethoden** nicht.

 

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

## <a name="members"></a>Member

Das **SWbemObjectSet-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemObjectSet-Objekt** verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Element**](swbemobjectset-item.md) | Ruft ein [**SWbemObject-Objekt**](swbemobject.md) aus der Auflistung ab. Dies ist die Standardmethode des -Objekts.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemObjectSet-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp          | BESCHREIBUNG                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Anzahl**](swbemobjectset-count.md)<br/>          | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/>        |
| [**Sicherheit\_**](swbemobjectset-security-.md)<br/> | Schreibgeschützt<br/> | Wird zum Lesen oder Ändern der Sicherheitseinstellungen verwendet.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein **SWbemObjectSet** ist eine Auflistung von null oder mehr [**SWbemObject-Objekten.**](swbemobject.md) Jedes **SWbemObject** in einem **SWbemObjectSet** kann eine von zwei Dingen darstellen:

-   Eine Instanz einer von WMI verwalteten Ressource.
-   Eine Instanz einer Klassendefinition.

Die gängigste Verwendung dieser Klasse in WMI ist als Rückgabewert für einen [**ExecQuery-**](/windows/desktop/api/Provider/nf-provider-provider-execquery) oder [**InstancesOf-Aufruf,**](swbemservices-instancesof.md) wie im folgenden Codebeispiel beschrieben:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



In den meisten Teilen werden Sie mit einem **SWbemObjectSet** nur alle Objekte auflisten, die in der Auflistung selbst enthalten sind. **SWbemObjectSet** enthält jedoch die Eigenschaft Count, die bei der Skripterstellung für die Systemverwaltung nützlich sein kann. Wie der Name schon sagt, gibt Count die Anzahl der Elemente in der Auflistung an. Dieses Skript ruft z. B. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:

Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md)

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel veranschaulicht, wie **SWbemObjectSet-Auflistungen** bearbeitet werden.


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



Das folgende Perl-Codebeispiel veranschaulicht, wie **SWbemObjectSet-Auflistungen** bearbeitet werden.


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




