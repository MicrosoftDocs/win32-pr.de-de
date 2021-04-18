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
# <a name="example-code-for-setting-an-ace-on-a-directory-object"></a><span data-ttu-id="1b16b-104">Beispiel Code für das Festlegen eines ACE für ein Verzeichnis Objekt</span><span class="sxs-lookup"><span data-stu-id="1b16b-104">Example Code for Setting an ACE on a Directory Object</span></span>

## <a name="define-the-setright-function"></a><span data-ttu-id="1b16b-105">Definieren der Funktion "settright"</span><span class="sxs-lookup"><span data-stu-id="1b16b-105">Define the SetRight function</span></span>

<span data-ttu-id="1b16b-106">Im folgenden Codebeispiel wird eine Funktion definiert, die einen Access Control Eintrag (ACE) zur freigegebenen Access Control Liste (DACL) der Sicherheits Beschreibung eines angegebenen Objekts in Active Directory Domain Services hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-106">The following code example defines a function that adds an Access Control Entry (ACE) to the Discretionary Access Control List (DACL) of the security descriptor of a specified object in Active Directory Domain Services.</span></span> <span data-ttu-id="1b16b-107">Die Unterroutine ermöglicht Ihnen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1b16b-107">The subroutine enables you to:</span></span>

-   <span data-ttu-id="1b16b-108">Gewähren oder Verweigern des Zugriffs auf das gesamte Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-108">Grant or deny access to the entire object.</span></span>
-   <span data-ttu-id="1b16b-109">Gewähren oder verweigern Sie den Zugriff auf eine bestimmte Eigenschaft für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-109">Grant or deny access to a specific property on the object.</span></span>
-   <span data-ttu-id="1b16b-110">Gewähren oder Verweigern des Zugriffs auf einen Satz von Eigenschaften für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-110">Grant or deny access to a set of properties on the object.</span></span>
-   <span data-ttu-id="1b16b-111">Erteilen oder verweigern Sie das Recht, einen bestimmten Typ eines untergeordneten Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b16b-111">Grant or deny the right to create a specific type of child object.</span></span>
-   <span data-ttu-id="1b16b-112">Legen Sie einen ACE fest, der von allen untergeordneten Objekten oder von untergeordneten Objekten einer angegebenen Objektklasse geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b16b-112">Set an ACE that can be inherited by all child objects or by child objects of a specified object class.</span></span>

<span data-ttu-id="1b16b-113">Im Anschluss an dieses Visual Basic Codebeispiel handelt es sich um mehrere Codebeispiele, die zeigen, wie die **SetRight** -Funktion verwendet wird, um verschiedene Arten von ACEs festzulegen</span><span class="sxs-lookup"><span data-stu-id="1b16b-113">Following this Visual Basic code example are several code examples that show how to use the **SetRight** function to set different types of ACEs.</span></span>


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



## <a name="grant-or-deny-access-to-the-entire-object"></a><span data-ttu-id="1b16b-114">Gewähren oder Verweigern des Zugriffs auf das gesamte Objekt</span><span class="sxs-lookup"><span data-stu-id="1b16b-114">Grant or deny access to the entire object</span></span>

<span data-ttu-id="1b16b-115">Im folgenden Visual Basic Codebeispiel wird eine Bindungs Zeichenfolge für den Benutzer Container erstellt und dann die **SetRight** -Funktion aufgerufen, um einen ACE für den Benutzer Container festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1b16b-115">The following Visual Basic code example builds a binding string for the Users container and then calls the **SetRight** function to set an ACE on the Users container.</span></span> <span data-ttu-id="1b16b-116">In diesem Beispiel wird ein ACE festgelegt, der dem Vertrauens nehmer das Recht gewährt, eine beliebige Eigenschaft für das Objekt zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b16b-116">This example sets an ACE that grants the trustee the right to read or write any property on the object.</span></span>


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



<span data-ttu-id="1b16b-117">Im folgenden C++-Codebeispiel wird ein ACE festgelegt, der dem Treuhänder die Berechtigung erteilt, eine beliebige Eigenschaft für das Objekt zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b16b-117">The following C++ code example sets an ACE that grants the trustee permission to read or write any property on the object.</span></span> <span data-ttu-id="1b16b-118">Im Codebeispiel wird davon ausgegangen, dass *pObject* und *sztreuhänder* auf gültige Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1b16b-118">The code example assumes that *pObject* and *szTrustee* are set to valid values.</span></span> <span data-ttu-id="1b16b-119">Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="1b16b-119">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>


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



## <a name="grant-or-deny-access-to-a-specific-property-on-the-object"></a><span data-ttu-id="1b16b-120">Gewähren oder Verweigern des Zugriffs auf eine bestimmte Eigenschaft für das Objekt</span><span class="sxs-lookup"><span data-stu-id="1b16b-120">Grant or deny access to a specific property on the object</span></span>

<span data-ttu-id="1b16b-121">In diesem Codebeispiel wird die **SetRight** -Funktion aufgerufen, um dem Vertrauens nehmer das Recht zu erteilen, eine bestimmte Eigenschaft für das Objekt zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b16b-121">This code example calls the **SetRight** function to grant the trustee the right to read or write a specific property on the object.</span></span> <span data-ttu-id="1b16b-122">Beachten Sie, dass Sie die " **schemaIdGUID** " der Eigenschaft angeben müssen, und Sie müssen das **Objekt "ADS \_ AceType \_ Access \_ Allowed \_** " angeben, um anzugeben, dass es sich hierbei um einen Objekt spezifischen ACE handelt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-122">Be aware that you must specify the **schemaIDGUID** of the property and you must specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span> <span data-ttu-id="1b16b-123">In diesem Codebeispiel wird auch das Flag " **\_ aceflag \_ erben- \_ ACE** " angegeben, das angibt, dass der ACE von untergeordneten Objekten geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b16b-123">This code example also specifies the **ADS\_ACEFLAG\_INHERIT\_ACE** flag which indicates that the ACE can be inherited by child objects.</span></span>


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



## <a name="grant-or-deny-access-to-a-set-of-properties-on-the-object"></a><span data-ttu-id="1b16b-124">Gewähren oder Verweigern des Zugriffs auf einen Satz von Eigenschaften für das Objekt</span><span class="sxs-lookup"><span data-stu-id="1b16b-124">Grant or deny access to a set of properties on the object</span></span>

<span data-ttu-id="1b16b-125">In diesem Codebeispiel wird die **SetRight** -Funktion aufgerufen, um dem Vertrauens nehmer das Recht zu erteilen, einen bestimmten Satz von Eigenschaften für das Objekt zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b16b-125">This code example calls the **SetRight** function to grant the trustee the right to read or write a specific set of properties on the object.</span></span> <span data-ttu-id="1b16b-126">Legen Sie den Zugriff auf das **Objekt "AD \_ AceType \_ Access \_ Allowed \_** " fest, um anzugeben, dass dies ein Objekt spezifischer ACE</span><span class="sxs-lookup"><span data-stu-id="1b16b-126">Specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span>

<span data-ttu-id="1b16b-127">Ein Eigenschaften Satz wird von einem **controlAccessRight** -Objekt im Container für erweiterte Rechte der Konfigurations Partition definiert.</span><span class="sxs-lookup"><span data-stu-id="1b16b-127">A property set is defined by a **controlAccessRight** object in the Extended Rights container of the Configuration partition.</span></span> <span data-ttu-id="1b16b-128">Um die im ACE festgelegte Eigenschaft zu identifizieren, geben Sie die **rightguid** -Eigenschaft eines **controlAccessRight** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1b16b-128">To identify the property set in the ACE, specify the **rightsGUID** property of a **controlAccessRight** object.</span></span> <span data-ttu-id="1b16b-129">Beachten Sie, dass diese Eigenschaften Satz-GUID auch in der **attributeSecurityGuid** -Eigenschaft jedes **attributeSchema** -Objekts festgelegt wird, das im Eigenschaften Satz enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1b16b-129">Be aware that this property set GUID is also set in the **attributeSecurityGUID** property of every **attributeSchema** object included in the property set.</span></span> <span data-ttu-id="1b16b-130">Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten](control-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="1b16b-130">For more information, see [Control Access Rights](control-access-rights.md).</span></span>

<span data-ttu-id="1b16b-131">Dieses Codebeispiel gibt auch Vererbungsflags an, die den ACE von untergeordneten Objekten als vererbbar festlegen, aber nicht für das unmittelbare Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b16b-131">This code example also specifies inheritance flags that set the ACE as inheritable by child objects, but ineffective on the immediate object.</span></span> <span data-ttu-id="1b16b-132">Außerdem gibt das Beispiel die GUID der User-Klasse an, die angibt, dass der ACE nur von Objekten dieser Klasse geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b16b-132">In addition, the sample specifies the GUID of the User class, which indicates that the ACE can be inherited only by objects of that class.</span></span>


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



## <a name="grant-or-deny-permission-to-create-a-specific-type-of-child-object"></a><span data-ttu-id="1b16b-133">Erteilen oder Verweigern der Berechtigung zum Erstellen eines bestimmten Typs von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="1b16b-133">Grant or deny permission to create a specific type of child object</span></span>

<span data-ttu-id="1b16b-134">Im folgenden Codebeispiel wird die **SetRight** -Funktion aufgerufen, um einem angegebenen Vertrauens nehmer das Recht zum Erstellen und Löschen von Benutzer Objekten in der Teilstruktur unter dem angegebenen-Objekt zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="1b16b-134">The following code example calls the **SetRight** function to grant a specified trustee the right to create and delete User objects in the subtree under the specified object.</span></span> <span data-ttu-id="1b16b-135">Beachten Sie, dass im Beispiel die GUID der User-Klasse angegeben wird, was bedeutet, dass der ACE nur dem Vertrauens nehmer ermöglicht, Benutzer Objekte zu erstellen, und keine Objekte anderer Klassen.</span><span class="sxs-lookup"><span data-stu-id="1b16b-135">Be aware that the sample specifies the GUID of the User class, which means that the ACE allows only the trustee to create User objects, not objects of other classes.</span></span> <span data-ttu-id="1b16b-136">Legen Sie den Zugriff auf das **Objekt "AD \_ AceType \_ Access \_ Allowed \_** " fest, um anzugeben, dass dies ein Objekt spezifischer ACE</span><span class="sxs-lookup"><span data-stu-id="1b16b-136">Specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span>


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



<span data-ttu-id="1b16b-137">Weitere Informationen und die Schema- **GUID** eines vordefinierten Attributs oder einer vordefinierten Klasse finden Sie auf der Referenzseite des-Attributs oder der-Klasse in der [Active Directory-Schema](/windows/desktop/ADSchema/active-directory-schema) Referenz.</span><span class="sxs-lookup"><span data-stu-id="1b16b-137">For more information, and the **schemaIDGUID** of a predefined attribute or class, see the attribute or class reference page in the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) reference.</span></span> <span data-ttu-id="1b16b-138">Weitere Informationen und ein Codebeispiel, das zum programmgesteuerten Abrufen einer **schemaIdGUID** verwendet werden kann, finden Sie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1b16b-138">For more information, and a code example that can be used to obtain a **schemaIDGUID** programmatically, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

 

 