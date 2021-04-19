---
title: Co-Branding von Online Stores
description: Co-Branding von Online Stores
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online Stores, Co-Branding
- Online Stores, Co-Branding
- Typ 1 Online Stores, Co-Branding
- Typ 2 Online Stores, Co-Branding
- Co-Branding von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339201"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="ff7ff-108">Co-Branding von Online Stores</span><span class="sxs-lookup"><span data-stu-id="ff7ff-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="ff7ff-109">Persönliche Computer OEMs, die keinen Musikspeicher betreiben, können mit Online Store-Anbietern mitmarken.</span><span class="sxs-lookup"><span data-stu-id="ff7ff-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="ff7ff-110">Das Windows Media Player-Setup unterstützt den Befehlszeilenparameter "serviceextra", damit Hardware OEMs ein benutzerdefiniertes Attribut festlegen können, das der Online Shop verwenden kann, um zu ermitteln, welcher OEM den ursprünglichen Online Store installiert hat</span><span class="sxs-lookup"><span data-stu-id="ff7ff-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="ff7ff-111">Wenn z. b. ein Computerhersteller mit dem Namen Fabrikam den anfänglichen Online Store auf den Proseware Music Store festlegen möchte, kann die folgende Befehlszeile zum Installieren von Windows Media Player 10 verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ff7ff-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="ff7ff-112">Wenn Windows Media Player auf diese Weise installiert wird, fügt der Player die serviceextra-Zeichenfolge jedes Mal an, wenn der Proseware-Dienst geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ff7ff-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="ff7ff-113">Das folgende Beispiel zeigt die URL, die von Windows Media Player an den Proseware-Dienst gesendet wird, um das serviceInfo-Dokument abzurufen:</span><span class="sxs-lookup"><span data-stu-id="ff7ff-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="ff7ff-114">Der Proseware Online Store kann dann mithilfe der Abfrage Zeichenfolge ermitteln, welche OEM-Media Player installierte Windows-und ein dynamisch generiertes serviceInfo-Dokument zurückgeben, das auf die Version des Online Stores mit dem Marken Format verweist.</span><span class="sxs-lookup"><span data-stu-id="ff7ff-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff7ff-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff7ff-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff7ff-116">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="ff7ff-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ff7ff-117">**Einrichten von Befehlszeilen Parametern für Online Stores**</span><span class="sxs-lookup"><span data-stu-id="ff7ff-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




