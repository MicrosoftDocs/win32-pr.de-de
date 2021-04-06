---
title: Verwenden eines ActiveX-Datenobjekts zum Binden an ADSI-Anbieter
description: Da ADSI auch ein OLE DB-Anbieter ist, können Sie ein ActiveX Data Object (ADO) zum Herstellen einer Verbindung mit ADSI-Anbietern verwenden.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX-Datenobjekt-ADSI
- ActiveX-Datenobjekt-ADSI, verwenden von ADO zum Binden an ADSI-Anbieter
- Dienstanbieter ADSI, verwenden des ActiveX-Datenobjekts zum Binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036295"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="0548a-106">Verwenden eines ActiveX-Datenobjekts zum Binden an ADSI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="0548a-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="0548a-107">Da ADSI auch ein OLE DB-Anbieter ist, können Sie ein ActiveX Data Object (ADO) zum Herstellen einer Verbindung mit ADSI-Anbietern verwenden.</span><span class="sxs-lookup"><span data-stu-id="0548a-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="0548a-108">Wie bei anderen ADO-Anbietern müssen Sie ein neues Verbindungs Objekt erstellen und optional die Anmelde Informationen angeben, um eine Verbindung mit einem OLE DB-Anbieter herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0548a-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="0548a-109">Der Name des ADSI-OLE DB Anbieters lautet **ADSDSOObject**.</span><span class="sxs-lookup"><span data-stu-id="0548a-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="0548a-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0548a-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="0548a-111">Im vorherigen Beispiel sind Sie im Namen des aktuellen Benutzers verbunden.</span><span class="sxs-lookup"><span data-stu-id="0548a-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="0548a-112">Um andere Anmelde Informationen anzugeben, verwenden Sie die Verbindungs Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0548a-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="0548a-113">ADSI OLE DB definiert die folgenden Verbindungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0548a-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="0548a-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0548a-114">Property</span></span>           | <span data-ttu-id="0548a-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0548a-115">Data type</span></span>   | <span data-ttu-id="0548a-116">Standard</span><span class="sxs-lookup"><span data-stu-id="0548a-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="0548a-117">"Benutzer-ID"</span><span class="sxs-lookup"><span data-stu-id="0548a-117">"User ID"</span></span>          | <span data-ttu-id="0548a-118">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="0548a-118">**BSTR**</span></span>    | <span data-ttu-id="0548a-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="0548a-119">**NULL**</span></span>  |
| <span data-ttu-id="0548a-120">Password</span><span class="sxs-lookup"><span data-stu-id="0548a-120">"Password"</span></span>         | <span data-ttu-id="0548a-121">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="0548a-121">**BSTR**</span></span>    | <span data-ttu-id="0548a-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="0548a-122">**NULL**</span></span>  |
| <span data-ttu-id="0548a-123">"Kennwort verschlüsseln"</span><span class="sxs-lookup"><span data-stu-id="0548a-123">"Encrypt Password"</span></span> | <span data-ttu-id="0548a-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="0548a-124">**BOOLEAN**</span></span> | <span data-ttu-id="0548a-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0548a-125">**FALSE**</span></span> |
| <span data-ttu-id="0548a-126">"ADSI-Flag"</span><span class="sxs-lookup"><span data-stu-id="0548a-126">"ADSI Flag"</span></span>        | <span data-ttu-id="0548a-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="0548a-127">**Long**</span></span>    | <span data-ttu-id="0548a-128">0</span><span class="sxs-lookup"><span data-stu-id="0548a-128">0</span></span>         |



 

<span data-ttu-id="0548a-129">Wenn Sie OLE DB ADO verwenden, können Sie keine Bindung an ein bestimmtes Objekt durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="0548a-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="0548a-130">Sie können jedoch ein bestimmtes Objekt Abfragen und ein Resultset zurückerhalten.</span><span class="sxs-lookup"><span data-stu-id="0548a-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="0548a-131">Nur ADSI-Anbieter, die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) unterstützen, profitieren von ADO als Programmiermodell.</span><span class="sxs-lookup"><span data-stu-id="0548a-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="0548a-132">Die Eigenschaft ADSI-Flag wird verwendet, um die Bindungs Authentifizierungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0548a-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="0548a-133">Bei dieser Eigenschaft kann es sich [**\_ \_ um**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) eine Kombination von Flags aus der Enumeration der ADS-Authentifizierungs Enumeration handeln.</span><span class="sxs-lookup"><span data-stu-id="0548a-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




