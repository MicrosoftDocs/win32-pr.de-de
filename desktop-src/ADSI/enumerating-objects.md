---
title: Auflisten von Objekten
description: Zum Anzeigen des untergeordneten Objekts eines Containers, z. b. einer Organisationseinheit (OE), zählen Sie das Container Objekt.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Auflisten von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855320"
---
# <a name="enumerating-objects"></a><span data-ttu-id="ff218-104">Auflisten von Objekten</span><span class="sxs-lookup"><span data-stu-id="ff218-104">Enumerating Objects</span></span>

<span data-ttu-id="ff218-105">Zum Anzeigen des untergeordneten Objekts eines Containers, z. b. einer Organisationseinheit (OE), zählen Sie das Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff218-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="ff218-106">Um eine Analogie zu einem Dateisystem zu erstellen, entspricht das untergeordnete Objekt den Dateien im Verzeichnis, während der Container, der das übergeordnete Objekt ist, dem Verzeichnis selbst entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff218-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="ff218-107">Sie können auch den auflisten-Vorgang verwenden, wenn Sie das übergeordnete Objekt eines Objekts abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="ff218-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="ff218-108">Wenn Sie ein Objekt auflisten, binden Sie tatsächlich an ein Objekt im Verzeichnis, und für jedes Objekt wird eine [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff218-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="ff218-109">Im folgenden Codebeispiel wird gezeigt, wie die untergeordneten Elemente eines Containers aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="ff218-109">The following code example shows how to enumerate the children of a container.</span></span>


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



<span data-ttu-id="ff218-110">Sie können die Typen von Objekten filtern, die von der-Enumeration zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff218-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="ff218-111">Wenn Sie z. b. nur Benutzer und Gruppen anzeigen möchten, verwenden Sie das folgende Codebeispiel vor der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ff218-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="ff218-112">Wenn Sie über einen Objekt Verweis verfügen, können Sie das übergeordnete Objekt des Objekts mit der über [**geordneten**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Eigenschaft erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff218-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="ff218-113">Im folgenden Codebeispiel wird gezeigt, wie eine Bindung an das übergeordnete Objekt erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="ff218-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="ff218-114">Weitere Informationen finden Sie unter Auflisten von [ADSI-Objekten](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ff218-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff218-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff218-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff218-116">Suchen nach Objekten</span><span class="sxs-lookup"><span data-stu-id="ff218-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




