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
# <a name="reading-the-schema"></a><span data-ttu-id="bd112-103">Lesen des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd112-103">Reading the Schema</span></span>

<span data-ttu-id="bd112-104">Die meisten Anbieter unterstützen das Schema, das mit Active Directory ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="bd112-104">Most providers support the schema that is shipped with Active Directory.</span></span> <span data-ttu-id="bd112-105">Das Schema enthält Klassen-und Attribut Definitionen.</span><span class="sxs-lookup"><span data-stu-id="bd112-105">The schema contains class and attribute definitions.</span></span> <span data-ttu-id="bd112-106">ADSI abstrahiert das Schema in "Provider://Schema".</span><span class="sxs-lookup"><span data-stu-id="bd112-106">ADSI abstracts the schema in "Provider://schema".</span></span> <span data-ttu-id="bd112-107">Jedes-Objekt enthält den Speicherort des Schemas, in dem die Klasse definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd112-107">Each object carries the schema location in which its class is defined.</span></span> <span data-ttu-id="bd112-108">Sie können diese Informationen mit der [**IADs:: get \_ Class**](iads-property-methods.md) -Eigenschaften Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="bd112-108">You can use the [**IADs::get\_Class**](iads-property-methods.md) property method to obtain this information.</span></span>

<span data-ttu-id="bd112-109">Gehen Sie folgendermaßen vor, um eine Bindung mit dem Schema Container in einer bestimmten Domäne herzustellen:</span><span class="sxs-lookup"><span data-stu-id="bd112-109">To bind to the schema container on a particular domain, do the following:</span></span>


```VB
Dim SchemaContainer As Object
Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
```


```C++

hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, IID_IADsContainer, (void**) &pSchema );
```





<span data-ttu-id="bd112-110">Zum Auflisten von Informationen im Schema Container binden Sie an den Container und zählen jedes Objekt im Container auf, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="bd112-110">To list information in the schema container, bind to the container and enumerate each object in the container as shown in the following:</span></span>


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





<span data-ttu-id="bd112-111">Sie können auch eine Bindung an ein-Objekt und den Speicherort des Schemas erhalten, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="bd112-111">You can also bind to an object and get the schema location, as shown in the following:</span></span>


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



 

 




