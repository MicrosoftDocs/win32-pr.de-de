---
description: Gibt das dem angegebenen Index zugeordnete Austausch Objekt in der Auflistung zurück.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Errbemubjectset. ItemIndex-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350067"
---
# <a name="swbemobjectsetitemindex-method"></a>Errbemubjectset. ItemIndex-Methode

Die **itemIndex** -Methode gibt das mit dem angegebenen Index verknüpfte [**Austausch Objekt**](swbemobject.md) in der Auflistung zurück. Der Index gibt die Position des Elements in der Auflistung an. Die Sammlungs Nummerierung beginnt bei Null.

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* 
</dt> <dd>

Der Index des Elements in der Auflistung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt das angeforderte [**Swap**](swbemobject.md) -Objekt zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der [**Element**](swbemobjectset-item.md) Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben. Dieser Fehler wird zurückgegeben, wenn eine negative Indexnummer angegeben wird.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der **itemIndex** -Methode können Skripts und Anwendungen von WMI-Clients, die in einer beliebigen Sprache geschrieben wurden, eine einheitliche Methode zum Bearbeiten einer Auflistung wie einem Array Diese Methode kann mit den [**Swap-Auflistungen von Swap-Objekte**](swbemobjectset.md) verwendet werden. Abfragen, wie z. b. " [**errbemservices. associatorsof**](swbemservices-associatorsof.md)", " [**errbemservices. referencesto**](swbemservices-referencesto.md)", " [**errbemservices. InstancesOf**](swbemservices-instancesof.md)" oder " [**SWbemServices.Execquery**](swbemservices-execquery.md) ", geben " **errbewbjectset** Collections Die **itemIndex** -Methode kann nicht mit Auflistungen verwendet werden, die keine Austausch Vorgänge enthalten, wie z. [**b**](swbemobject.md). " [**errbemmethodset**](swbemmethodset.md)", " [**errbemnamedvalueset**](swbemnamedvalueset.md)", " [**errbemprivilegeset**](swbemprivilegeset.md)", " [**taubempropertyset**](swbempropertyset.md)" und " [**errbemqualifierset**](swbemqualifierset.md)".

**ItemIndex** kann auch zum Abrufen der einzelnen Instanz einer Singleton-Klasse verwendet werden.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird eine Auflistung aller Win32- [**\_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Instanzen abgefragt. Anschließend werden die Namen der ersten drei Prozesse angezeigt.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Für jede Betriebssystem Installation ist nur eine Instanz des [**Win32- \_ OperatingSystems**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) vorhanden. Das Erstellen des [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) -Pfads zum Abrufen der einzelnen Instanz ist umständlich, sodass Skripts das **Win32- \_ OperatingSystem** normalerweise auflisten, auch wenn nur eine Instanz verfügbar ist. Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie die **itemIndex** -Methode verwendet wird, um ein **Win32- \_ OperatingSystem** ohne Verwendung einer **for each** -Schleife zu erhalten.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



Im folgenden VBScript-Codebeispiel werden die dem [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)zugeordneten Instanzen abgerufen, z. b. [**Win32 \_ systemoperatingsystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



Die folgende Codebeispiel Ausgabe zeigt die Instanzen, die mit dem [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)verknüpft sind.

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
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

[**Austauschen von "errbemubjectset"**](swbemobjectset.md)
</dt> </dl>

 

