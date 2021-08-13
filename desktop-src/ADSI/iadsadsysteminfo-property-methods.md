---
title: IADsADSystemInfo-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsADSystemInfo-Schnittstelle erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- IADsADSystemInfo-Eigenschaftsmethoden ADSI
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
ms.openlocfilehash: 177926924d989686dae33c3403c07bfe5e69d0ba1762dd2a1a1cdee78a2175f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691611"
---
# <a name="iadsadsysteminfo-property-methods"></a>IADsADSystemInfo-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADsADSystemInfo-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**ComputerName**
</dt> <dd> <dl>

Ruft den Distinguished Name des lokalen Computers ab.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Ruft den DNS-Namen der Domäne des lokalen Computers ab, z. B. "domainName.companyName.com".

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**DomainShortName**
</dt> <dd> <dl>

Ruft den Kurznamen der Domäne des lokalen Computers ab, z. B. "domainName".

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**IsNativeMode**
</dt> <dd> <dl>

Bestimmt, ob sich die Domäne des lokalen Computers im nativ oder gemischten Modus befindet.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BOOL**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

**PDCRoleOwner**
</dt> <dd> <dl>

Ruft den Distinguished Name des DSA-Objekts (Directory Service Agent) für den Domänencontroller ab, der die primäre Domänencontrollerrolle in der Domäne des lokalen Computers besitzt.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Ruft den Distinguished Name des Verzeichnisdienst-Agent-Objekts (DSA) für den Domänencontroller ab, der die Schemamasterrolle in der Gesamtstruktur des lokalen Computers besitzt.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Skriptdatentyp: **BSTR**
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

Ruft den Active Directory-Distinguished Name des aktuellen Benutzers ab. Dabei handelt es sich um den angemeldeten Benutzer oder den Benutzer, dessen Identität vom aufrufenden Thread angenommen wird.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden C++-Codebeispiel werden die Windows abgerufen. Aus Kürze wird die Fehlerüberprüfung weggelassen.


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



Im folgenden Visual Basic Codebeispiel werden Windows Systeminformationen abgerufen.


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



Im folgenden VBScript/ASP-Codebeispiel werden die Windows abgerufen.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsADSystemInfo ist als 5BB11929-AFD1-11D2-9CB9-0000F87A369E definiert.<br/>     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

