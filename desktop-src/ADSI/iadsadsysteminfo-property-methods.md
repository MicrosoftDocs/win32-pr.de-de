---
title: IADsADSystemInfo-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsADSystemInfo-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- IADsADSystemInfo-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105165"
---
# <a name="iadsadsysteminfo-property-methods"></a>IADsADSystemInfo-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Computername**
</dt> <dd> <dl>

Ruft den Distinguished Name des lokalen Computers ab.

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

**DomainDNSName**
</dt> <dd> <dl>

Ruft den DNS-Namen der Domäne des lokalen Computers ab, z. b. "domainname.CompanyName.com".

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**Domainshortname**
</dt> <dd> <dl>

Ruft den Kurznamen der Domäne des lokalen Computers ab, z. b. "Domänen Name".

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

**ForestDNSName**
</dt> <dd> <dl>

Ruft den DNS-Namen der Gesamtstruktur des lokalen Computers ab.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**Isnativemode**
</dt> <dd> <dl>

Bestimmt, ob sich die Domäne des lokalen Computers im einheitlichen oder gemischten Modus befindet.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

**PdcRoleOwner**
</dt> <dd> <dl>

Ruft den Distinguished Name des Verzeichnisdienst-Agent-Objekts (DSA) für den Domänen Controller ab, der die Rolle des primären Domänen Controllers in der Domäne des lokalen Computers besitzt.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**SchemaRoleOwner**
</dt> <dd> <dl>

Ruft den Distinguished Name des Verzeichnisdienst-Agent-Objekts (DSA) für den Domänen Controller ab, der die Schema Master Rolle in der Gesamtstruktur des lokalen Computers besitzt.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**Sitename**
</dt> <dd> <dl>

Ruft den Standortnamen des lokalen Computers ab.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

**UserName**
</dt> <dd> <dl>

Ruft den Active Directory Distinguished Name des aktuellen Benutzers ab, der der angemeldete Benutzer ist, oder der Benutzer, der vom aufrufenden Thread angenommen wird.

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

Im folgenden C++-Codebeispiel werden die Windows-Systeminformationen abgerufen. Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



Im folgenden Visual Basic Codebeispiel werden die Windows-Systeminformationen abgerufen.


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



Im folgenden VBScript/ASP-Codebeispiel werden die Windows-Systeminformationen abgerufen.


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsADSystemInfo ist als 5bb11929-afd1-11d2-9cb9-0000f87a369e definiert.<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

