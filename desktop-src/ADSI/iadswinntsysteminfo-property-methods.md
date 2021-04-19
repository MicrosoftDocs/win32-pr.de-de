---
title: Iadswinntsysteminfo-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadswinntsysteminfo-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Iadswinntsysteminfo-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337907"
---
# <a name="iadswinntsysteminfo-property-methods"></a>Iadswinntsysteminfo-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadswinntsysteminfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Computername**
</dt> <dd> <dl>

Der Name des Host Computers, auf dem die Anwendung ausgeführt wird.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**DomainName**
</dt> <dd> <dl>

Der Name der Domäne, zu der der Benutzer gehört.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

**PDC**
</dt> <dd> <dl>

Der Name des primären Domänen Controllers, zu dem der Host Computer gehört.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

**UserName**
</dt> <dd> <dl>

Der Name des Benutzerkontos, unter dem das **winntsysteminfo** -Objekt erstellt wird.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden C/C++-Codebeispiel werden die WinNT-Systeminformationen abgerufen. Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



Im folgenden Visual Basic Codebeispiel werden die WinNT-Systeminformationen abgerufen.


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



Im folgenden Codebeispiel für Visual Basic Scripting Edition/Active Server Pages werden die WinNT-Systeminformationen abgerufen.


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadswinntsysteminfo ist als 6c6d65dc-afd1-11d2-9cb9-0000f 87a369e definiert.<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadswinntsysteminfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





