---
title: IADs-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADs-Schnittstelle erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen zu Eigenschaftenmethoden finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- IADs-Eigenschaftsmethoden ADSI
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
ms.openlocfilehash: 3326bbbf5ea7c2d2a98a6224f9b0a83a738c76a206d343a8629138d4d45e73b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082524"
---
# <a name="iads-property-methods"></a>IADs-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen zu Eigenschaftenmethoden finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge dieses Objekts. Die Zeichenfolge identifiziert dieses Objekt in einer Netzwerkumgebung eindeutig. Das -Objekt kann immer mit diesem Pfad abgerufen werden.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Der Name der Objektschemaklasse.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Der global eindeutige Bezeichner des Verzeichnisobjekts. Die [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) konvertiert die **GUID** aus einer Oktettzeichenfolge, die auf einem Verzeichnisserver gespeichert ist, in ein Zeichenfolgenformat.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Der relative Name des Objekts, wie im zugrunde liegenden Verzeichnisdienst benannt. Dieser Name unterscheidet dieses Objekt von seinen gleichgeordneten Objekten.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Die ADsPath-Zeichenfolge des übergeordneten Containers. Active Directory lässt die Bildung des ADsPath eines bestimmten Objekts nicht zu, indem die Eigenschaften **Parent** und **Name verkettet** werden. Obwohl dieser Vorgang bei einigen Anbietern funktionieren kann, ist es nicht garantiert, dass er für alle Implementierungen funktioniert. Der ADsPath ist garantiert gültig und sollte immer zum Abrufen des Schnittstellenzeigers eines Objekts verwendet werden.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Die ADsPath-Zeichenfolge des Schemaklassenobjekts dieses Objekts.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

In Active Directory ist die **von GUID** zurückgegebene GUID eine Zeichenfolge mit Hexadezimalen. Verwenden Sie die resultierende **GUID,** um eine direkte Bindung an das Objekt zu erstellen.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



Wobei xxx der wert ist, der von der GUID-Eigenschaft zurückgegeben wird. Weitere Informationen finden Sie unter [Verwenden von objectGUID zum Binden an ein Objekt.](/windows/desktop/AD/using-objectguid-to-bind-to-an-object) Beachten Sie, dass bei Verwendung einer GUID zum Binden an ein Objekt die **ADsPath-Eigenschaftsmethode** Werte zurückgibt, die sich von den normalen Werten unterscheiden, die zurückgegeben werden, wenn Sie einen Distinguished Name (DN) zum Binden an dasselbe Objekt verwendet haben. In der folgenden Tabelle werden beispielsweise die Werte aufgeführt, die zurückgegeben werden, wenn die beiden verschiedenen Bindungsmethoden zum Binden an dasselbe Benutzerobjekt verwendet werden.



|             | Binden mithilfe von DN                                           | Binden mithilfe der GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Name**    | CN=Jeff Smith                                           | CN=Jeff Smith                                               |
| **Parent**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com | LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> Der WinNT-Anbieter unterstützt keine Bindung mithilfe der **Objekt-GUID** und gibt die **GUID-Eigenschaft** in einem etwas anderen Zeichenfolgenformat zurück.

 

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie Objektdaten mithilfe von Eigenschaftsmethoden der [**IADs-Schnittstelle abgerufen**](/windows/desktop/api/Iads/nn-iads-iads) werden.


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



Das folgende Codebeispiel zeigt, wie Objektdaten mithilfe von Eigenschaftsmethoden der [**IADs-Schnittstelle abgerufen**](/windows/desktop/api/Iads/nn-iads-iads) werden.


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



Das folgende Codebeispiel zeigt, wie sie mit den Eigenschaftenmethoden der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) arbeiten.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | \_IID-IADs sind als FD8256D0-FD15-11CE-ABC4-02608C9E7553 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

