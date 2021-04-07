---
title: Lesen des Schemas
description: Die meisten Anbieter unterstützen das Schema, das mit Active Directory ausgeliefert wird.
ms.assetid: cc35789e-5cfe-49e9-9fb3-489b949768c5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091d225c1be90d887f6994eda782ad7a7adb65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855256"
---
# <a name="reading-the-schema"></a>Lesen des Schemas

Die meisten Anbieter unterstützen das Schema, das mit Active Directory ausgeliefert wird. Das Schema enthält Klassen-und Attribut Definitionen. ADSI abstrahiert das Schema in "Provider://Schema". Jedes-Objekt enthält den Speicherort des Schemas, in dem die Klasse definiert ist. Sie können diese Informationen mit der [**IADs:: get \_ Class**](iads-property-methods.md) -Eigenschaften Methode abrufen.

Gehen Sie folgendermaßen vor, um eine Bindung mit dem Schema Container in einer bestimmten Domäne herzustellen:


```VB
Dim SchemaContainer As Object
Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
```


```C++

hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, IID_IADsContainer, (void**) &pSchema );
```





Zum Auflisten von Informationen im Schema Container binden Sie an den Container und zählen jedes Objekt im Container auf, wie im folgenden dargestellt:


```VB
Dim prop As Object
Dim obj As Object
Dim SchemaContainer As Object
Dim Class As Object

Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
'Show all items in the schema container
For Each obj In SchemaContainer
     Debug.Print obj.Name & " (" & obj.Class & ")"
Next

'Show the optional attributes
For Each prop In Class.OptionalProperties
   Debug.Print prop
Next
```


```C++

IADsContainer *pSchema=NULL;
 HRESULT hr;

 CoInitialize(NULL);

 hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, 
                   IID_IADsContainer, (void**) &pSchema );

 if ( !SUCCEEDED(hr) )
 {
   return hr;
 }

 // Enumerate schema objects
 IEnumVARIANT *pEnum = NULL;
 hr = ADsBuildEnumerator( pSchema, &pEnum );
 pSchema->Release(); // This is no longer needed, since we have the enumerator already.
    
 if ( SUCCEEDED(hr) )
 {
   VARIANT var;
   ULONG lFetch;
   IADs *pChild=NULL;
   VariantInit(&var);
        
   while( SUCCEEDED(ADsEnumerateNext( pEnum, 1, &var, &lFetch )) && lFetch == 1 )
   {
     hr = V_DISPATCH(&var)->QueryInterface( IID_IADs, (void**) &pChild );
     if ( SUCCEEDED(hr) )
     {
       BSTR bstrName;
       BSTR bstrClass;
       // Get more information on the child classes
       pChild->get_Name(&bstrName);
       pChild->get_Class(&bstrClass);
                
       printf(&quot;%S\t\t(%S)\n&quot;, bstrName, bstrClass );
                
       // Clean-up
       SysFreeString(bstrName);
       SysFreeString(bstrClass);
                
       pChild->Release();
     }
     VariantClear(&var);
   }
 }

 CoUninitialize();
```





Sie können auch eine Bindung an ein-Objekt und den Speicherort des Schemas erhalten, wie im folgenden dargestellt:


```VB
Dim prop As Object
Dim dom As Object
Dim Class As Object

Set dom = GetObject("LDAP://Fabrikam")
Debug.Print dom.Schema
Set Class = GetObject(dom.Schema)
'Mandatory attributes
For Each prop In Class.MandatoryProperties
    Debug.Print prop
Next
```



 

 




