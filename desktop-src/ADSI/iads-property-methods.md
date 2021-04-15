---
title: IADs-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADs-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- IADs-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517432"
---
# <a name="iads-property-methods"></a><span data-ttu-id="aa05f-105">IADs-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="aa05f-105">IADs Property Methods</span></span>

<span data-ttu-id="aa05f-106">Mit den Eigenschafts Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa05f-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="aa05f-107">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="aa05f-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="aa05f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa05f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="aa05f-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="aa05f-109">**ADsPath**</span></span>
<span data-ttu-id="aa05f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-111">Die ADsPath-Zeichenfolge dieses-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa05f-111">The ADsPath string of this object.</span></span> <span data-ttu-id="aa05f-112">Die Zeichenfolge identifiziert dieses Objekt eindeutig in einer Netzwerkumgebung.</span><span class="sxs-lookup"><span data-stu-id="aa05f-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="aa05f-113">Das Objekt kann immer mit diesem Pfad abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="aa05f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-115">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa05f-116">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa05f-116">**Class**</span></span>
<span data-ttu-id="aa05f-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-118">Der Name der Objekt Schema Klasse.</span><span class="sxs-lookup"><span data-stu-id="aa05f-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="aa05f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-120">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa05f-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="aa05f-121">**GUID**</span></span>
<span data-ttu-id="aa05f-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-123">Die Globally Unique Identifier des Verzeichnis Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa05f-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="aa05f-124">Die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle konvertiert die **GUID** aus einer Oktett-Zeichenfolge, die auf einem Verzeichnisserver gespeichert ist, in ein Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="aa05f-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="aa05f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-126">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa05f-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa05f-127">**Name**</span></span>
<span data-ttu-id="aa05f-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-129">Der relative Name des-Objekts, das im zugrunde liegenden Verzeichnisdienst benannt ist.</span><span class="sxs-lookup"><span data-stu-id="aa05f-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="aa05f-130">Dieser Name unterscheidet dieses Objekt von seinen gleich geordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="aa05f-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="aa05f-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-132">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa05f-133">**Parent**</span><span class="sxs-lookup"><span data-stu-id="aa05f-133">**Parent**</span></span>
<span data-ttu-id="aa05f-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-135">Die ADsPath-Zeichenfolge des übergeordneten Containers.</span><span class="sxs-lookup"><span data-stu-id="aa05f-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="aa05f-136">Active Directory lässt die Erstellung des ADsPath eines bestimmten Objekts nicht zu, indem die über **geordneten** Eigenschaften und die **Name** -Eigenschaft verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="aa05f-137">Dieser Vorgang kann zwar bei manchen Anbietern funktionieren, aber es ist nicht gewährleistet, dass er für alle Implementierungen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aa05f-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="aa05f-138">Der ADsPath ist garantiert gültig und sollte immer zum Abrufen des Schnittstellen Zeigers eines Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="aa05f-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-140">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa05f-141">**Schema**</span><span class="sxs-lookup"><span data-stu-id="aa05f-141">**Schema**</span></span>
<span data-ttu-id="aa05f-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aa05f-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="aa05f-143">Die ADsPath-Zeichenfolge des Schema Klassen Objekts dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa05f-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="aa05f-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa05f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa05f-145">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aa05f-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="aa05f-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa05f-146">Remarks</span></span>

<span data-ttu-id="aa05f-147">In Active Directory ist die **GUID** , die von GUID zurückgegeben wird, eine Zeichenfolge von hexadedezimalen.</span><span class="sxs-lookup"><span data-stu-id="aa05f-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="aa05f-148">Verwenden Sie die resultierende **GUID** , um direkt an das Objekt zu binden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="aa05f-149">Dabei ist xxx der Wert, der von der GUID-Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa05f-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="aa05f-150">Weitere Informationen finden Sie unter [Verwenden von objectGUID für die Bindung an ein-Objekt](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="aa05f-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="aa05f-151">Beachten Sie, dass die **ADsPath** -Eigenschaften Methode, wenn Sie eine GUID für die Bindung an ein Objekt verwenden, Werte zurückgibt, die sich von den normalen Werten unterscheiden, die zurückgegeben werden, wenn Sie einen Distinguished Name (DN) zum Binden an dasselbe Objekt verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="aa05f-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="aa05f-152">In der folgenden Tabelle sind z. b. die Werte aufgeführt, die zurückgegeben werden, wenn die beiden unterschiedlichen Bindungsmethoden zum Binden an dasselbe Benutzerobjekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="aa05f-153">Binden mithilfe von DN</span><span class="sxs-lookup"><span data-stu-id="aa05f-153">Bind using DN</span></span>                                           | <span data-ttu-id="aa05f-154">Bindung mithilfe der GUID</span><span class="sxs-lookup"><span data-stu-id="aa05f-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="aa05f-155">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa05f-155">**Name**</span></span>    | <span data-ttu-id="aa05f-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="aa05f-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="aa05f-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="aa05f-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="aa05f-158">**Parent**</span><span class="sxs-lookup"><span data-stu-id="aa05f-158">**Parent**</span></span>  | <span data-ttu-id="aa05f-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="aa05f-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="aa05f-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="aa05f-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="aa05f-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="aa05f-161">**ADsPath**</span></span> | <span data-ttu-id="aa05f-162">LDAP://Server/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="aa05f-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="aa05f-163">LDAP://Server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="aa05f-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="aa05f-164">Der WinNT-Anbieter unterstützt keine Bindung mithilfe der Objekt- **GUID** und gibt die **GUID** -Eigenschaft in einem etwas anderen Zeichen folgen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="aa05f-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="aa05f-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa05f-165">Examples</span></span>

<span data-ttu-id="aa05f-166">Im folgenden Codebeispiel wird gezeigt, wie Objektdaten mithilfe von Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="aa05f-167">Im folgenden Codebeispiel wird gezeigt, wie Objektdaten mithilfe von Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa05f-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="aa05f-168">Im folgenden Codebeispiel wird gezeigt, wie Sie mit den Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle arbeiten.</span><span class="sxs-lookup"><span data-stu-id="aa05f-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="aa05f-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa05f-169">Requirements</span></span>



| <span data-ttu-id="aa05f-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa05f-170">Requirement</span></span> | <span data-ttu-id="aa05f-171">Wert</span><span class="sxs-lookup"><span data-stu-id="aa05f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa05f-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa05f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="aa05f-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa05f-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa05f-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa05f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="aa05f-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa05f-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa05f-176">Header</span><span class="sxs-lookup"><span data-stu-id="aa05f-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa05f-177"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa05f-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="aa05f-178">DLL</span><span class="sxs-lookup"><span data-stu-id="aa05f-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa05f-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa05f-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa05f-180">IID</span><span class="sxs-lookup"><span data-stu-id="aa05f-180">IID</span></span><br/>                      | <span data-ttu-id="aa05f-181">IID \_ IADs ist als FD8256D0-FD15-11CE-ABC4-02608C9E7553 definiert.</span><span class="sxs-lookup"><span data-stu-id="aa05f-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="aa05f-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa05f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa05f-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="aa05f-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="aa05f-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="aa05f-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

