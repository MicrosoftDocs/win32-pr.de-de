---
title: Beispiel Code für das Festlegen eines ACE für ein Verzeichnis Objekt
description: Dieses Thema enthält mehrere Codebeispiele, in denen der DACL (diskreAccess Control List) der Sicherheits Beschreibung eines Verzeichnis Objekts ein Access Control Eintrag (ACE) hinzugefügt wird.
ms.assetid: fb1ad9f5-af2f-4ad1-a58b-6439cca6fd23
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Festlegen eines ACE für ein Verzeichnis Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16180a2e1216c749c35d68ff607e81320a1482c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106337837"
---
# <a name="example-code-for-setting-an-ace-on-a-directory-object"></a>Beispiel Code für das Festlegen eines ACE für ein Verzeichnis Objekt

## <a name="define-the-setright-function"></a>Definieren der Funktion "settright"

Im folgenden Codebeispiel wird eine Funktion definiert, die einen Access Control Eintrag (ACE) zur freigegebenen Access Control Liste (DACL) der Sicherheits Beschreibung eines angegebenen Objekts in Active Directory Domain Services hinzufügt. Die Unterroutine ermöglicht Ihnen Folgendes:

-   Gewähren oder Verweigern des Zugriffs auf das gesamte Objekt.
-   Gewähren oder verweigern Sie den Zugriff auf eine bestimmte Eigenschaft für das Objekt.
-   Gewähren oder Verweigern des Zugriffs auf einen Satz von Eigenschaften für das Objekt.
-   Erteilen oder verweigern Sie das Recht, einen bestimmten Typ eines untergeordneten Objekts zu erstellen.
-   Legen Sie einen ACE fest, der von allen untergeordneten Objekten oder von untergeordneten Objekten einer angegebenen Objektklasse geerbt werden kann.

Im Anschluss an dieses Visual Basic Codebeispiel handelt es sich um mehrere Codebeispiele, die zeigen, wie die **SetRight** -Funktion verwendet wird, um verschiedene Arten von ACEs festzulegen


```VB
Const ACL_REVISION_DS = &H4

Public Function SetRight(objectDN As String, _
               accessrights As Long, _
               accesstype As Long, _
               aceinheritflags As Long, _
               objectGUID As String, _
               inheritedObjectGUID As String, _
               trustee As String) As Boolean
             
Dim dsobject As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim newace As New AccessControlEntry
Dim lflags As Long

On Error GoTo Cleanup
 
' Bind to the specified object.
Set dsobject = GetObject(objectDN)
 
' Read the security descriptor on the object.
Set sd = dsobject.Get("ntSecurityDescriptor")
 
' Get the DACL from the security descriptor.
Set dacl = sd.DiscretionaryAcl
 
' Set the properties of the new ACE.
newace.AccessMask = accessrights
newace.AceType = accesstype
newace.AceFlags = aceinheritflags
newace.trustee = trustee
 
' Set the GUID for the object type or inherited object type.
lflags = 0

If Not objectGUID = vbNullString Then
   newace.ObjectType = objectGUID
   lflags = lflags Or &H1 'ADS_FLAG_OBJECT_TYPE_PRESENT
End If

If Not inheritedObjectGUID = vbNullString Then
   newace.InheritedObjectType = inheritedObjectGUID
   lflags = lflags Or &H2 'ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT
End If

If Not (lflags = 0) Then newace.Flags = lflags
 
' Set the ACL Revision.
dacl.AclRevision = ACL_REVISION_DS

' Add the ACE to the DACL and to the security descriptor.
dacl.AddAce newace
sd.DiscretionaryAcl = dacl
 
' Apply it to the object.
dsobject.Put "ntSecurityDescriptor", sd
dsobject.SetInfo
SetRight = True
Exit Function

Cleanup:
Set dsobject = Nothing
Set sd = Nothing
Set dacl = Nothing
Set newace = Nothing
SetRight = False

End Function
```




```C++
HRESULT SetRight(
          IADs *pObject,
          long lAccessMask,
          long lAccessType,
          long lAccessInheritFlags,
          LPOLESTR szObjectGUID,
          LPOLESTR szInheritedObjectGUID,
          LPOLESTR szTrustee)
{
VARIANT varSD;
HRESULT hr = E_FAIL;
IADsAccessControlList *pACL = NULL;
IADsSecurityDescriptor *pSD = NULL;
IDispatch *pDispDACL = NULL;
IADsAccessControlEntry *pACE = NULL;
IDispatch *pDispACE = NULL;
long lFlags = 0L;
 
// The following code example takes the szTrustee in an expected naming format 
// and assumes it is the name for the correct trustee.
// The application should validate the specified trustee.
if (!szTrustee || !pObject)
    return E_INVALIDARG;
 
VariantInit(&varSD);
 
// Get the nTSecurityDescriptor.
// Type should be VT_DISPATCH - an IDispatch pointer to the security descriptor object.
hr = pObject->Get(_bstr_t("nTSecurityDescriptor"), &varSD);
if ( FAILED(hr) || varSD.vt != VT_DISPATCH ) {
    wprintf(L"get nTSecurityDescriptor failed: 0x%x\n", hr);
    return hr;
}
 
hr = V_DISPATCH( &varSD )->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if ( FAILED(hr) ) {
    wprintf(L"QueryInterface for IADsSecurityDescriptor failed: 0x%x\n", hr);
    goto cleanup;
}
 
// Get the DACL.
hr = pSD->get_DiscretionaryAcl(&pDispDACL);
if (SUCCEEDED(hr)) 
    hr = pDispDACL->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if ( FAILED(hr) ) {
    wprintf(L"Could not get DACL: 0x%x\n", hr);
    goto cleanup;
}
 
// Create the COM object for the new ACE.
hr  = CoCreateInstance( 
               CLSID_AccessControlEntry,
               NULL,
               CLSCTX_INPROC_SERVER,
               IID_IADsAccessControlEntry,
               (void **)&pACE
               );
if ( FAILED(hr) ) {
    wprintf(L"Could not create ACE object: 0x%x\n", hr);
    goto cleanup;
}
 
// Set the properties for the new ACE.
 
// Set the mask that specifies the access right.
hr = pACE->put_AccessMask( lAccessMask );
 
// Set the trustee.
hr = pACE->put_Trustee( szTrustee );
 
// Set AceType.
hr = pACE->put_AceType( lAccessType );
 
// Set AceFlags to specify whether other objects can inherit the ACE from the specified object.
hr = pACE->put_AceFlags( lAccessInheritFlags );
 
// If an szObjectGUID is specified, add ADS_FLAG_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the ObjectType.
if (szObjectGUID)
{
    lFlags |= ADS_FLAG_OBJECT_TYPE_PRESENT;
    hr = pACE->put_ObjectType( szObjectGUID );
}
 
// If an szInheritedObjectGUID is specified, add ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the InheritedObjectType.
if (szInheritedObjectGUID)
{
    lFlags |= ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT;
    hr = pACE->put_InheritedObjectType( szInheritedObjectGUID );
}
 
// Set flags if ObjectType or InheritedObjectType were set.
if (lFlags)
    hr = pACE->put_Flags(lFlags);
 
// Add the ACE to the ACL to the SD to the cache to the object.
// Call the QueryInterface method for the IDispatch pointer to pass to the AddAce method.
hr = pACE->QueryInterface(IID_IDispatch, (void**)&pDispACE);
if (SUCCEEDED(hr))
{
    // Set the ACL revision.
    hr = pACL->put_AclRevision(ACL_REVISION_DS);

    // Add the ACE.
    hr = pACL->AddAce(pDispACE);
    if (SUCCEEDED(hr))
    {
        // Write the DACL.
        hr = pSD->put_DiscretionaryAcl(pDispDACL);
        if (SUCCEEDED(hr))
        {
            // Write the ntSecurityDescriptor property to the property cache.
            hr = pObject->Put(CComBSTR("nTSecurityDescriptor"), varSD);
            if (SUCCEEDED(hr))
            {
                // Call SetInfo to update the property on the object in the directory.
                hr = pObject->SetInfo();
            }
        }
    }
}
 
cleanup:
if (pDispACE)
    pDispACE->Release();
if (pACE)
    pACE->Release();
if (pACL)
    pACL->Release();
if (pDispDACL)
    pDispDACL->Release();
if (pSD)
    pSD->Release();
 
VariantClear(&varSD);
return hr;
}
```



## <a name="grant-or-deny-access-to-the-entire-object"></a>Gewähren oder Verweigern des Zugriffs auf das gesamte Objekt

Im folgenden Visual Basic Codebeispiel wird eine Bindungs Zeichenfolge für den Benutzer Container erstellt und dann die **SetRight** -Funktion aufgerufen, um einen ACE für den Benutzer Container festzulegen. In diesem Beispiel wird ein ACE festgelegt, der dem Vertrauens nehmer das Recht gewährt, eine beliebige Eigenschaft für das Objekt zu lesen oder zu schreiben.


```VB
Dim rootDSE As IADs
Dim objectDN As String
Dim bResult As Boolean
Const ADS_RIGHT_READ_PROP = &H10
Const ADS_RIGHT_WRITE_PROP = &H20
 
' Bind to the Users container in the local domain.
Set rootDSE = GetObject("LDAP://rootDSE")
objectDN = "LDAP://cn=users," & rootDSE.Get("defaultNamingContext")
 
' Grant trustee the right to read/write any property.
bResult = SetRight objectDN, _
  ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
   ADS_ACETYPE_ACCESS_ALLOWED, _
    0, _
    vbNullString, _
    vbNullString, _
    "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write any property.")
Else
    MsgBox ("An error occurred.")
End If
```



Im folgenden C++-Codebeispiel wird ein ACE festgelegt, der dem Treuhänder die Berechtigung erteilt, eine beliebige Eigenschaft für das Objekt zu lesen oder zu schreiben. Im Codebeispiel wird davon ausgegangen, dass *pObject* und *sztreuhänder* auf gültige Werte festgelegt sind. Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).


```C++
HRESULT hr;
IADs *pObject;
LPWSTR szTrustee;
 
hr = SetRight(
          pObject,  // IADs pointer to the object
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED,
          0,        // Not inheritable
          NULL,     // No object type GUID
          NULL,     // No inherited object type GUID
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-specific-property-on-the-object"></a>Gewähren oder Verweigern des Zugriffs auf eine bestimmte Eigenschaft für das Objekt

In diesem Codebeispiel wird die **SetRight** -Funktion aufgerufen, um dem Vertrauens nehmer das Recht zu erteilen, eine bestimmte Eigenschaft für das Objekt zu lesen oder zu schreiben. Beachten Sie, dass Sie die " **schemaIdGUID** " der Eigenschaft angeben müssen, und Sie müssen das **Objekt "ADS \_ AceType \_ Access \_ Allowed \_** " angeben, um anzugeben, dass es sich hierbei um einen Objekt spezifischen ACE handelt. In diesem Codebeispiel wird auch das Flag " **\_ aceflag \_ erben- \_ ACE** " angegeben, das angibt, dass der ACE von untergeordneten Objekten geerbt werden kann.


```VB
' Grant trustee the right to read the Telephone-Number property
' of all child objects in the Users container. 
' {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
' the Telephone-Number property.

bResult = SetRight objectDN, _
     ADS_RIGHT_WRITE_PROP Or ADS_RIGHT_READ_PROP, _
     ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
      ADS_ACEFLAG_INHERIT_ACE, _
       "{bf967a49-0de6-11d0-a285-00aa003049e2}", _
       vbNullString, _
       "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read the telephone number property.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read the Telephone-Number property
// of all child objects in the Users container. 
// {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
// the Telephone-Number property.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE,
          L"{bf967a49-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-set-of-properties-on-the-object"></a>Gewähren oder Verweigern des Zugriffs auf einen Satz von Eigenschaften für das Objekt

In diesem Codebeispiel wird die **SetRight** -Funktion aufgerufen, um dem Vertrauens nehmer das Recht zu erteilen, einen bestimmten Satz von Eigenschaften für das Objekt zu lesen oder zu schreiben. Legen Sie den Zugriff auf das **Objekt "AD \_ AceType \_ Access \_ Allowed \_** " fest, um anzugeben, dass dies ein Objekt spezifischer ACE

Ein Eigenschaften Satz wird von einem **controlAccessRight** -Objekt im Container für erweiterte Rechte der Konfigurations Partition definiert. Um die im ACE festgelegte Eigenschaft zu identifizieren, geben Sie die **rightguid** -Eigenschaft eines **controlAccessRight** -Objekts an. Beachten Sie, dass diese Eigenschaften Satz-GUID auch in der **attributeSecurityGuid** -Eigenschaft jedes **attributeSchema** -Objekts festgelegt wird, das im Eigenschaften Satz enthalten ist. Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten](control-access-rights.md).

Dieses Codebeispiel gibt auch Vererbungsflags an, die den ACE von untergeordneten Objekten als vererbbar festlegen, aber nicht für das unmittelbare Objekt. Außerdem gibt das Beispiel die GUID der User-Klasse an, die angibt, dass der ACE nur von Objekten dieser Klasse geerbt werden kann.


```VB
' Grant trustee permission to read or write a set of properties.
' {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
' a property set.
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class, so this ACE is inherited only by objects of that class.

bResult = SetRight objectDN, _
        ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
          ADS_ACEFLAG_INHERIT_ACE Or ADS_ACEFLAG_INHERIT_ONLY_ACE, _
          "{77B5B886-944A-11d1-AEBD-0000F80367C1}", _
          "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
          "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write a set of properties.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read or write a set of properties.
// {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
// a property set (rightsGUID of a controlAccessRight object).
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class, so this ACE is inherited only by objects of that class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE,
          L"{77B5B886-944A-11d1-AEBD-0000F80367C1}",
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          szTrustee
          );
```



## <a name="grant-or-deny-permission-to-create-a-specific-type-of-child-object"></a>Erteilen oder Verweigern der Berechtigung zum Erstellen eines bestimmten Typs von untergeordneten Objekten

Im folgenden Codebeispiel wird die **SetRight** -Funktion aufgerufen, um einem angegebenen Vertrauens nehmer das Recht zum Erstellen und Löschen von Benutzer Objekten in der Teilstruktur unter dem angegebenen-Objekt zu gewähren. Beachten Sie, dass im Beispiel die GUID der User-Klasse angegeben wird, was bedeutet, dass der ACE nur dem Vertrauens nehmer ermöglicht, Benutzer Objekte zu erstellen, und keine Objekte anderer Klassen. Legen Sie den Zugriff auf das **Objekt "AD \_ AceType \_ Access \_ Allowed \_** " fest, um anzugeben, dass dies ein Objekt spezifischer ACE


```VB
' Grant trustee the right to create or delete User objects 
' in the specified object. 
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class.

bResult = SetRight objectDN, _
          ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD, _
           ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
           0, _
           "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
           vbNullString, _
           "jeffsmith@fabrikam.com" 'trustee

If bResult = True Then
    MsgBox ("The trustee can create or delete User objects.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to create or delete User objects 
// in the specified object. 
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_DS_CREATE_CHILD | ADS_RIGHT_DS_DELETE_CHILD,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          0,        // Not inheritable.
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



Weitere Informationen und die Schema- **GUID** eines vordefinierten Attributs oder einer vordefinierten Klasse finden Sie auf der Referenzseite des-Attributs oder der-Klasse in der [Active Directory-Schema](/windows/desktop/ADSchema/active-directory-schema) Referenz. Weitere Informationen und ein Codebeispiel, das zum programmgesteuerten Abrufen einer **schemaIdGUID** verwendet werden kann, finden Sie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md).

 

 