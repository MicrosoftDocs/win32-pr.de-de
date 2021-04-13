---
title: Schnittstellen für Server Datenobjekte
description: Die Server Data Objects (SDO)-API macht die folgenden Schnittstellen verfügbar.
ms.assetid: c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0c5105194056e70855c390c40011075c7718a7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391120"
---
# <a name="server-data-objects-interfaces"></a><span data-ttu-id="13935-103">Schnittstellen für Server Datenobjekte</span><span class="sxs-lookup"><span data-stu-id="13935-103">Server Data Objects Interfaces</span></span>

<span data-ttu-id="13935-104">Die Server Data Objects (SDO)-API macht die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13935-104">The Server Data Objects (SDO) API exposes the following interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13935-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="13935-105">Interface</span></span></th>
<th><span data-ttu-id="13935-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="13935-106">Purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13935-107"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdo"><strong>Isdo</strong></a></span><span class="sxs-lookup"><span data-stu-id="13935-107"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdo"><strong>ISdo</strong></a></span></span></td>
<td><span data-ttu-id="13935-108">Bearbeiten eines SDO-Objekts.</span><span class="sxs-lookup"><span data-stu-id="13935-108">Manipulate an SDO object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13935-109"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection"><strong>Isdocollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="13935-109"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection"><strong>ISdoCollection</strong></a></span></span></td>
<td><span data-ttu-id="13935-110">Bearbeitet eine Auflistung von SDO-Objekten.</span><span class="sxs-lookup"><span data-stu-id="13935-110">Manipulate a collection of SDO objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13935-111"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold"><strong>Isdodiktattionaryold</strong></a></span><span class="sxs-lookup"><span data-stu-id="13935-111"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold"><strong>ISdoDictionaryOld</strong></a></span></span></td>
<td><span data-ttu-id="13935-112">Bearbeiten Sie das Attribut Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="13935-112">Manipulate the attribute dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13935-113"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine"><strong>Isdomachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="13935-113"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine"><strong>ISdoMachine</strong></a></span></span></td>
<td><span data-ttu-id="13935-114">Verwalten des SDO-Computers und Abrufen von SDO-Objekten.</span><span class="sxs-lookup"><span data-stu-id="13935-114">Manage the SDO computer, and retrieve SDO objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13935-115"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol"><strong>Isdoservicecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="13935-115"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol"><strong>ISdoServiceControl</strong></a></span></span></td>
<td><span data-ttu-id="13935-116">Verwalten Sie den verwalteten Dienst über SDO, d. h. entweder Internet Authentifizierungsdienst (IAS) oder RAS-Server (RAS).</span><span class="sxs-lookup"><span data-stu-id="13935-116">Manage the service being administered through SDO, that is, either Internet Authentication Service (IAS) or Remote Access Server (RAS).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="13935-117">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="13935-117">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

