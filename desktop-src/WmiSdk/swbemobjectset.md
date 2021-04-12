---
description: Ein errbemubjectset-Objekt ist eine Auflistung von Swap-Objekten. Weitere Informationen finden Sie unter Zugreifen auf eine Sammlung. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Errbemubjectset-Objekt (wbemdisp. h)
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
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218294"
---
# <a name="swbemobjectset-object"></a>Errbemubjectset-Objekt

Ein **errbemubjectset** -Objekt ist eine Auflistung von [**Swap**](swbemobject.md) -Objekten. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md). Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.

Sie können ein Objekt von " **errbemubjectset** " abrufen, indem Sie eine der folgenden Methoden oder deren asynchrone Entsprechungen aufrufen:

-   [**"Errbemujeject. ASSOCIATORS"\_**](swbemobject-associators-.md)
-   [**"Errbemubject. Instance"\_**](swbemobject-instances-.md)
-   [**"Errbemubject. References"\_**](swbemobject-references-.md)
-   [**Swap. subclasses\_**](swbemobject-subclasses-.md)
-   [**"Taubemservices. associatorsof"**](swbemservices-associatorsof.md)
-   [**CquerySWbemServices.Exe**](swbemservices-execquery.md)
-   [**Swap Services. InstancesOf**](swbemservices-instancesof.md)
-   [**"Swap Services. referencesto"**](swbemservices-referencesto.md)
-   [**Swap Services. SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> Das Objekt " **errbemubjectset** " unterstützt die optionalen **Add** -und **Remove** -Auflistungs Methoden nicht.

 

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, empfiehlt es sich, anstelle der asynchronen Kommunikation semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

## <a name="members"></a>Member

Das " **errbeporbjectset** "-Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **errbemubjectset** " verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Element**](swbemobjectset-item.md) | Ruft [**ein-**](swbemobject.md) Objekt aus der-Auflistung ab. Dies ist die Standardmethode des-Objekts.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **errbemubjectset** " verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp          | BESCHREIBUNG                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Countdown**](swbemobjectset-count.md)<br/>          | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/>        |
| [**Sicherheit\_**](swbemobjectset-security-.md)<br/> | Schreibgeschützt<br/> | Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein " **errbemubjectset** " ist eine Auflistung von 0 (null) oder mehr " [**errbejebject**](swbemobject.md) "-Objekten. Jedes "Swap"- **Objekt** in einem " **errbemubjectset** " kann eine der beiden folgenden Punkte darstellen:

-   Eine Instanz einer von WMI verwalteten Ressource.
-   Eine Instanz einer Klassendefinition.

Diese Klasse wird am häufigsten in WMI als Rückgabewert für einen [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) -oder [**InstancesOf**](swbemservices-instancesof.md) -Rückruf verwendet, wie im folgenden Codebeispiel beschrieben:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



Der einzige Schritt, den Sie jemals mit einem " **errbemubjectset** " ausführen, ist das Auflisten aller Objekte, die in der Auflistung enthalten sind. Allerdings enthält " **errbewbjectset** " eine Eigenschaften Anzahl, die bei der Skripterstellung für die System Administration nützlich sein kann. Wie der Name schon sagt, gibt count die Anzahl der Elemente in der Auflistung an. Dieses Skript ruft z. b. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:

Weitere Informationen zur Verwendung dieser Klasse finden Sie unter Auflisten von [WMI](enumerating-wmi.md).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie die Austausch Vorgänge von " **errbewbjectset** " manipuliert werden.


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



Im folgenden perl-Codebeispiel wird veranschaulicht, wie die **Swap-Auflistungen von Swap**


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Objekt Satz<br/>                                                        |
| IID<br/>                      | IID \_ iswbemubjectset<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




