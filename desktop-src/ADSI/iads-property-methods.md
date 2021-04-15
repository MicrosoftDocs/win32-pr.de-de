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
# <a name="iads-property-methods"></a>IADs-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge dieses-Objekts. Die Zeichenfolge identifiziert dieses Objekt eindeutig in einer Netzwerkumgebung. Das Objekt kann immer mit diesem Pfad abgerufen werden.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Klasse**
</dt> <dd> <dl>

Der Name der Objekt Schema Klasse.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

Die Globally Unique Identifier des Verzeichnis Objekts. Die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle konvertiert die **GUID** aus einer Oktett-Zeichenfolge, die auf einem Verzeichnisserver gespeichert ist, in ein Zeichen folgen Format.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Name**
</dt> <dd> <dl>

Der relative Name des-Objekts, das im zugrunde liegenden Verzeichnisdienst benannt ist. Dieser Name unterscheidet dieses Objekt von seinen gleich geordneten Elementen.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Parent**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge des übergeordneten Containers. Active Directory lässt die Erstellung des ADsPath eines bestimmten Objekts nicht zu, indem die über **geordneten** Eigenschaften und die **Name** -Eigenschaft verkettet werden. Dieser Vorgang kann zwar bei manchen Anbietern funktionieren, aber es ist nicht gewährleistet, dass er für alle Implementierungen funktioniert. Der ADsPath ist garantiert gültig und sollte immer zum Abrufen des Schnittstellen Zeigers eines Objekts verwendet werden.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Schema**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge des Schema Klassen Objekts dieses Objekts.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

In Active Directory ist die **GUID** , die von GUID zurückgegeben wird, eine Zeichenfolge von hexadedezimalen. Verwenden Sie die resultierende **GUID** , um direkt an das Objekt zu binden.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



Dabei ist xxx der Wert, der von der GUID-Eigenschaft zurückgegeben wird. Weitere Informationen finden Sie unter [Verwenden von objectGUID für die Bindung an ein-Objekt](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Beachten Sie, dass die **ADsPath** -Eigenschaften Methode, wenn Sie eine GUID für die Bindung an ein Objekt verwenden, Werte zurückgibt, die sich von den normalen Werten unterscheiden, die zurückgegeben werden, wenn Sie einen Distinguished Name (DN) zum Binden an dasselbe Objekt verwendet haben. In der folgenden Tabelle sind z. b. die Werte aufgeführt, die zurückgegeben werden, wenn die beiden unterschiedlichen Bindungsmethoden zum Binden an dasselbe Benutzerobjekt verwendet werden.



|             | Binden mithilfe von DN                                           | Bindung mithilfe der GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Name**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **Parent**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://Server/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com | LDAP://Server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> Der WinNT-Anbieter unterstützt keine Bindung mithilfe der Objekt- **GUID** und gibt die **GUID** -Eigenschaft in einem etwas anderen Zeichen folgen Format zurück.

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie Objektdaten mithilfe von Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle abgerufen werden.


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



Im folgenden Codebeispiel wird gezeigt, wie Objektdaten mithilfe von Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle abgerufen werden.


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



Im folgenden Codebeispiel wird gezeigt, wie Sie mit den Eigenschaften Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle arbeiten.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADs ist als FD8256D0-FD15-11CE-ABC4-02608C9E7553 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

