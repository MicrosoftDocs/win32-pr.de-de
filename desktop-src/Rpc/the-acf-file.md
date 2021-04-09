---
title: Die ACF-Datei
description: Mithilfe der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client-und/oder Server Anwendungen anpassen, ohne dass sich dies auf die Netzwerk Merkmale der Schnittstelle auswirkt.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949070"
---
# <a name="the-acf-file"></a><span data-ttu-id="b14c2-103">Die ACF-Datei</span><span class="sxs-lookup"><span data-stu-id="b14c2-103">The ACF File</span></span>

<span data-ttu-id="b14c2-104">Mithilfe der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client-und/oder Server Anwendungen anpassen, ohne dass sich dies auf die Netzwerk Merkmale der Schnittstelle auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b14c2-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="b14c2-105">Wenn Ihre Client Anwendung z. b. eine komplexe Datenstruktur enthält, die nur auf dem lokalen Computer Bedeutung hat, können Sie in der ACF-Datei angeben, wie die Daten in dieser Struktur in einem Computer unabhängigen Formular für Remote Prozedur Aufrufe dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="b14c2-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="b14c2-106">Dieses Tutorial veranschaulicht eine weitere Verwendung der ACF-Datei – gibt den Typ des Bindungs Handles an, das die Verbindung zwischen Client und Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="b14c2-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="b14c2-107">Mit dem **\[** [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) - **\]** Attribut im ACF-Header kann die Client Anwendung einen Server für den Remote Prozedur aufzurufen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b14c2-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="b14c2-108">Der ACF definiert das Handle, das vom [**Typhandle \_ t**](/windows/desktop/Midl/handle-t) (ein primitiver primitiver Datentyp) sein soll.</span><span class="sxs-lookup"><span data-stu-id="b14c2-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="b14c2-109">Der mittlerer l-Compiler fügt den von der ACF angegebenen Bindungs Handle-Namen, Hello \_ ifhandle, in die von ihm generierte Header Datei ein.</span><span class="sxs-lookup"><span data-stu-id="b14c2-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="b14c2-110">Beachten Sie, dass diese bestimmte ACF-Datei einen leeren Text enthält.</span><span class="sxs-lookup"><span data-stu-id="b14c2-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="b14c2-111">Der mittlerer l-Compiler verfügt über die Option [**/App \_ config**](/windows/desktop/Midl/-app-config), mit der Sie bestimmte ACF-Attribute (z. b. **implizites \_ handle**) in die IDL-Datei einschließen können, anstatt eine separate ACF-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b14c2-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="b14c2-112">Verwenden Sie diese Option, wenn für Ihre Anwendung keine sehr spezielle Konfiguration erforderlich ist und die strikte OSF-Kompatibilität kein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="b14c2-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 