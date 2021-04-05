---
title: Iadscomputer-Eigenschaften Methoden (IADs. h)
description: Die iadscomputer-Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Iadscomputer-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859116"
---
# <a name="iadscomputer-property-methods"></a>Iadscomputer-Eigenschaften Methoden

Die [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) -Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Computer-ID**
</dt> <dd> <dl>

Die den einzelnen Computern zugewiesenen Globally Unique Identifier.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

**Abteilung**
</dt> <dd> <dl>

Die Organisationseinheit (OU), z. b. die Abteilung, zu der dieser Computer gehört.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

**Beschreibung**
</dt> <dd> <dl>

Die Beschreibung dieses Computers.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**Division**
</dt> <dd> <dl>

Die Division innerhalb einer Organisation, der dieser Computer angehört.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

**Location**
</dt> <dd> <dl>

Der zugewiesene physische Speicherort dieses Computers.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

**MemorySize**
</dt> <dd> <dl>

Die Größe des zufälligen zugriffsspeichers für diesen Computer in Megabyte.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

**Modell**
</dt> <dd> <dl>

Die Marke und das Modell dieses Computers.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

**Netzwerkadressen**
</dt> <dd> <dl>

Ein Array von netaddress-Feldern, die die Adressen darstellen, von denen dieser Computer erreicht werden kann. Netaddress ist ein Anbieter spezifisches **BSTR** , bestehend aus zwei Teil Zeichenfolgen, die durch einen Doppelpunkt (:) getrennt sind. Die linke Teil Zeichenfolge gibt den Adresstyp an, und die Rechte Teil Zeichenfolge ist eine Zeichen folgen Darstellung einer Adresse dieses Typs. Beispielsweise weisen TCP/IP-Adressen folgendes Format auf: IP: 100.201.301.45. Die IPX-typadressen weisen folgendes Format auf: IPX: 10.123456.80.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

**OperatingSystem**
</dt> <dd> <dl>

Das auf diesem Computer verwendete Betriebssystem.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

**OperatingSystemVersion**
</dt> <dd> <dl>

Die Version des Betriebssystems, das auf diesem Computer verwendet wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

**Besitzer**
</dt> <dd> <dl>

Die Person, der dieser Computer zugewiesen ist. Diese Person sollte auch über eine Lizenz zum Ausführen der installierten Software verfügen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**PrimaryUser**
</dt> <dd> <dl>

Der Name der Kontaktperson (z. b. ein Administrator) für diesen Computer.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

**Prozessor**
</dt> <dd> <dl>

Der Prozessortyp.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

**ProcessorCount**
</dt> <dd> <dl>

Die Anzahl der installierten Prozessoren.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

**Rolle**
</dt> <dd> <dl>

Die Rolle dieses Computers, z. b. Arbeitsstation, Server oder Domänen Controller.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

**Website**
</dt> <dd> <dl>

Der Globally Unique Identifier, der den Standort identifiziert, in dem dieser Computer installiert wurde. Bei einem Standort handelt es sich um eine physische Region der guten Konnektivität in einem Netzwerk.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

**Storagecapacity**
</dt> <dd> <dl>

Die Größe des Datenträgers in Megabyte.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

Verschiedene Anbieter können unterschiedliche Eigenschaften eines Computer Objekts verfügbar machen. Weitere Informationen finden Sie unter [ADSI-System Anbieter](adsi-system-providers.md).

Sie können ermitteln, welche Eigenschaften unterstützt werden, indem Sie die obligatorischen und optionalen Eigenschaften über die zugehörige Schema Klasse überprüfen. Weitere Informationen finden Sie unter [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle.

Wenn Sie den Status eines Computers überprüfen oder den Vorgang zum Herunterfahren über das Netzwerk ausführen möchten, müssen Sie die [**iadscomputeroperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) -Schnittstelle verwenden.

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel werden Computer Eigenschaften überprüft, die vom ADSI WinNT-Anbieter unterstützt werden.


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



Im folgenden C++-Codebeispiel werden Computer Eigenschaften überprüft, die vom ADSI WinNT-Anbieter unterstützt werden.


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadscomputer ist als EFE3CC70-1D9F-11CF-B1F3-02608C9E7553 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[ADSI-System Anbieter](adsi-system-providers.md)
</dt> <dt>

[**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**Iadscomputeroperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





