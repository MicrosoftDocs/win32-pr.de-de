---
title: IADsAccessControlList-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsAccessControlList-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften ermittelt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: cb68bb61-4216-4f69-bea1-ab7f98937a27
ms.tgt_platform: multiple
keywords:
- IADsAccessControlList-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlList Property Methods
- IADsAccessControlList.AclRevision
- IADsAccessControlList.get_AclRevision
- IADsAccessControlList.put_AclRevision
- IADsAccessControlList.AceCount
- IADsAccessControlList.get_AceCount
- IADsAccessControlList.put_AceCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55763b7c52071ca5bfd0a875912941090b7992c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391650"
---
# <a name="iadsaccesscontrollist-property-methods"></a>IADsAccessControlList-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften ermittelt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Acecount**
</dt> <dd> <dl>

Die Anzahl der Zugriffs Steuerungs Einträge in der Zugriffs Steuerungs Liste.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceCount(
  [out] LONG* lnAceCount
);
HRESULT put_AceCount(
  [in] LONG lnAceCount
);
```


</dt> </dl> </dd> <dt>

**Aclrevision**
</dt> <dd> <dl>

Die Revisions Ebene einer Zugriffs Steuerungs Liste. Dieser Wert kann eine **ACL- \_ Revision** oder **ACL- \_ Revision \_** sein. Verwenden Sie **ACL \_ Revision \_ DS** , wenn die ACL einen Objekt spezifischen ACE enthält. Alle ACEs in einer ACL müssen die gleiche Revisions Ebene aufweisen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AclRevision(
  [out] LONG* lnAclRevision
);
HRESULT put_AclRevision(
  [in] LONG lnAclRevision
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Anzahl von ACEs in einer ACL angezeigt.


```VB
Dim x as IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup

Set x = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Debug.Print Dacl.AceCount

Cleanup:
    If (Err.Number <> 0) Then
        MsgBox ("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
```



Im folgenden Codebeispiel wird die Anzahl von ACEs in einer ACL angezeigt.


```C++
HRESULT ShowACEInACL(LPWSTR guestPath,LPWSTR user,LPWSTR passwd)
{
  IADs *pObj = NULL;
  IADsSecurityDescriptor *psd = NULL;
  HRESULT hr = S_OK;
  VARIANT var;

  VariantInit(&var);

  hr = ADsOpenObject(guestPath,user,passwd,ADS_SECURE_AUTHENTICATION,
                     IID_IADs,(void**)&pObj);
  if(FAILED(hr)) {
      printf("hr = %x\n",hr);
      return hr;
  }
  else {
      BSTR bstr = NULL;
      pObj->get_Class(&bstr);
      printf("Object class: %S\n",bstr);
      SysFreeString(bstr);
  }

  hr = pObj->Get(CComBSTR("ntSecurityDescriptor"), &var);
  pObj->Release();

  if(FAILED(hr)) {
      printf("Get ntSD: hr = %x\n",hr);
      return hr;
  }

  hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,
                                        (void**)&psd);

  if(FAILED(hr)) {
      printf("DISP: hr = %x\n",hr);
      VariantClear(&var);
      return hr;
  }

  IDispatch *pDisp = NULL;
  hr = psd->get_DiscretionaryAcl(&pDisp);
  VariantClear(&var);

  if(FAILED(hr)) {
      printf("get_DACL : hr = %x\n",hr);
      return hr;
  }

  IADsAccessControlList *pAcl = NULL;
  hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pAcl);
  pDisp->Release();

  if(FAILED(hr)) {
      printf("QI ACL: hr = %x\n",hr);
      return hr;
  }

  long count = 0;
  hr = pAcl->get_AceCount(&count);
  pAcl->Release();
  if(FAILED(hr)) {
      printf("Count: hr = %x\n",hr);
      return hr;
  }

  printf("AceCount = %d\n",count);

  return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsAccessControlList ist als B7EE91CC-9BDD-11D0-852C-00C04FD8D503 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

