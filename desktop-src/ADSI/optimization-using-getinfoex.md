---
title: Optimierung mithilfe von "GetInfoEx"
description: Wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimierung mit GetInfoEx ADSI
- GetInfoEx ADSI, Optimierung mithilfe von IADs GetInfoEx
- ADSI ADSI, using, Optimierung mithilfe der IADs GetInfoEx-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316454"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="ba8ff-106">Optimierung mithilfe von "GetInfoEx"</span><span class="sxs-lookup"><span data-stu-id="ba8ff-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="ba8ff-107">Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="ba8ff-108">Diese Methode lädt nur die angegebenen Attributwerte in den lokalen Cache.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="ba8ff-109">Die [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode wird verwendet, um alle Attributwerte in den lokalen Cache zu laden.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="ba8ff-110">Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode ruft bestimmte aktuelle Werte für die Eigenschaften eines Active Directory Objekts aus dem zugrunde liegenden Verzeichnis Speicher ab und aktualisiert die zwischengespeicherten Werte.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="ba8ff-111">Wenn bereits ein Wert im Eigenschafts Cache vorhanden ist, wird der zwischengespeicherte Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis abgerufen, wenn die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -oder [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode aufgerufen wird, ohne dass zuerst " [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) " für dieses Attribut aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="ba8ff-112">Dies kann bewirken, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, die Werte jedoch nicht mit einem Aufrufen der [**IADs. \* tinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode in den zugrunde liegenden Verzeichnisdienst übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="ba8ff-113">Die empfohlene Methode zur Vermeidung von zwischen Speicherungs Problemen besteht darin, die Attribut Wertänderungen immer zu übertragen, indem **IADs. SetInfo** aufgerufen wird, bevor [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)aufgerufen wird</span><span class="sxs-lookup"><span data-stu-id="ba8ff-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="ba8ff-114">Abrufen Active Directory konstruierter Attribute</span><span class="sxs-lookup"><span data-stu-id="ba8ff-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="ba8ff-115">In Active Directory werden die meisten konstruierten Attribute abgerufen und zwischengespeichert, wenn die [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aufgerufen wird ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) führt einen impliziten **IADs. GetInfo** -Aufruf aus, wenn der Cache leer ist).</span><span class="sxs-lookup"><span data-stu-id="ba8ff-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="ba8ff-116">Einige konstruierte Attribute werden jedoch nicht automatisch abgerufen und zwischengespeichert. Daher ist es erforderlich, dass die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode explizit aufgerufen wird, um Sie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="ba8ff-117">In Active Directory wird das Attribut [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) beispielsweise nicht abgerufen, wenn die **IADs. GetInfo** -Methode aufgerufen wird und **IADs. Get** die **E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="ba8ff-118">Die **IADs. GetInfoEx** -Methode muss aufgerufen werden, um das **CanonicalName** -Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="ba8ff-119">Diese konstruierten Attribute werden auch nicht mithilfe der [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle zum Auflisten der Attribute abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba8ff-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="ba8ff-120">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie alle Attributwerte abrufen, finden Sie unter [Beispielcode zum Lesen eines konstruierten Attributs](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="ba8ff-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 