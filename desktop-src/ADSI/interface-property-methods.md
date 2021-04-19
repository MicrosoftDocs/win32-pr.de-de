---
title: Schnittstelleneigenschaften Methoden
description: Viele ADSI-Schnittstellen dienen zur Unterstützung der Automatisierung und sind daher duale Schnittstellen darin, dass Sie den Client Zugriff über IUnknown-und IDispatch-Schnittstellen unterstützen.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Schnittstelleneigenschaften Methoden
- ADSI ADSI, Referenz, Eigenschaften Methoden erläutert
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342376"
---
# <a name="interface-property-methods"></a><span data-ttu-id="59c31-105">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="59c31-105">Interface Property Methods</span></span>

<span data-ttu-id="59c31-106">Viele ADSI-Schnittstellen dienen zur Unterstützung der Automatisierung und sind daher duale Schnittstellen darin, dass Sie den Client Zugriff über [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -und [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="59c31-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="59c31-107">Nicht Automatisierungs Clients, wie z. b. in C/C++ geschriebene Clients, lösen den Methodenaufruf direkt mithilfe der [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode aus, und die Methode wird direkt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="59c31-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="59c31-108">Automatisierungs Clients, auch als namens gebundene Clients bezeichnet (z. b. in Visual Basic oder Visual Basic Scripting Edition (VBScript)), müssen den Methodenaufruf indirekt mit der [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) -Methode auflösen.</span><span class="sxs-lookup"><span data-stu-id="59c31-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="59c31-109">Eine ADSI-Schnittstelle zur Unterstützung der Automatisierung definiert Eigenschaften Methoden zum Abrufen und Ändern von Eigenschaften eines Objekts, das die-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="59c31-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="59c31-110">Die Eigenschaften Methoden haben Namen, denen " **Get** " \_ und " **Put** " \_ die entsprechenden Eigenschaften Namen vorangestellt sind, z. b. " **get \_ User** " und " **Put \_ Name**".</span><span class="sxs-lookup"><span data-stu-id="59c31-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="59c31-111">Jede **get \_** -Methode nimmt einen einzelnen Parameter als Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="59c31-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="59c31-112">Dieser Parameter ist eine von der Methode zugewiesene Adresse einer Variablen des Eigenschafts Datentyps.</span><span class="sxs-lookup"><span data-stu-id="59c31-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="59c31-113">Bei der Rückgabe nimmt diese Variable den aktuellen Wert der angeforderten Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="59c31-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="59c31-114">Der Aufrufer muss den zugewiesenen Speicher der Variablen freigeben, wenn die Eigenschaft nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="59c31-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="59c31-115">Jede **Put \_** -Methode nimmt einen einzelnen Parameter als Eingabe für den Datentyp der entsprechenden Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="59c31-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="59c31-116">Der-Parameter enthält einen neuen Wert der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="59c31-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="59c31-117">Im folgenden Codebeispiel wird der Aufruf der-Eigenschaften Methoden veranschaulicht, die der üblichen Prozedur folgen, um die Member-Funktion eines Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="59c31-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="59c31-118">Im folgenden Codebeispiel wird der Aufruf der-Eigenschaften Methoden in Automatisierungs Clients veranschaulicht, die sich etwas unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="59c31-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="59c31-119">Beispielsweise Visual Basic die Punkt Notation verwendet.</span><span class="sxs-lookup"><span data-stu-id="59c31-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="59c31-120">Alle Parameter und Rückgabe Typen müssen die Werte aufweisen, die der Variant-Datentyp definiert.</span><span class="sxs-lookup"><span data-stu-id="59c31-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="59c31-121">Alle Methoden für eine duale Schnittstelle geben einen HRESULT-Wert zurück, um einen Erfolg oder Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="59c31-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="59c31-122">Weitere Informationen zum erhalten und Festlegen von Eigenschaften für ADSI-Objekte finden Sie unter [Property Cache](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="59c31-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 