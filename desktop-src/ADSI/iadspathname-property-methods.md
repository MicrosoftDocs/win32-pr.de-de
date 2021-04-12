---
title: Iadspathname-Eigenschaften Methoden (IADs. h)
description: Die escapedmode-Eigenschaften werden abgerufen oder festgelegt.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Iadspathname-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213728"
---
# <a name="iadspathname-property-methods"></a>Iadspathname-Eigenschaften Methoden

Die Eigenschaften Methoden der [**iadspathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) -Schnittstelle ruft die **escapedmode** -Eigenschaften ab oder legt Sie fest. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Escapedmode**
</dt> <dd> <dl>

Überprüfen oder angeben, wie Escapezeichen in einem Pfadnamen behandelt werden. Weitere Informationen und definierte Optionen finden Sie unter [**ADS-escapemodusenum \_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

Der **escapedmode** stellt einen Status dar. Sie können diese aktivieren bzw. deaktivieren, indem Sie Sie auf ADS \_ escapedmode \_ on oder ADS \_ escapedmode \_ Off/ADS \_ escapedmode \_ Off \_ per festlegen. Wenn Sie aktiviert oder deaktiviert ist, werden alle nachfolgenden Abruf Zeichen mit Escapezeichen oder ohne Escapezeichen versehen.

In ADSI ist nur der [**iadspathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) in der Lage, Pfade zu vermeiden. Alle anderen ADSI-Schnittstellen geben immer escapepfade zurück. Der Standardzustand von " **escapedmode** " lautet "ADS \_ escapedmode default" gemäß \_ Definition in der ADS-escapesequenzenum. [**\_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie die **escapedmode** -Eigenschaft zum Aktivieren/Deaktivieren der folgenden drei Sonderzeichen verwendet wird: "=", "," und "/".


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



Im folgenden Codebeispiel wird gezeigt, wie die **escapedmode** -Eigenschaft zum Aktivieren/Deaktivieren der folgenden drei Sonderzeichen verwendet wird: "=", "," und "/".


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **escapedmode** -Eigenschaft arbeiten. Die Fehlerüberprüfung wird ignoriert.


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadspathname ist als D592AED4-F420-11D0-A36E-00C04FB950DC definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[**ADS \_ - \_ escapesmodusenum \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





