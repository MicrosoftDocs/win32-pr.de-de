---
title: ServiceInfo-Dokument für einen Typ-1-Online Store
description: ServiceInfo-Dokument für einen Typ-1-Online Store
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037109"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="6dc47-107">ServiceInfo-Dokument für einen Typ-1-Online Store</span><span class="sxs-lookup"><span data-stu-id="6dc47-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="6dc47-108">Typ 1 Online Stores müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Online Shop beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6dc47-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="6dc47-109">In Windows Media Player 11 wird dieses Dokument verwendet, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Online Stores konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="6dc47-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="6dc47-110">Das serviceInfo-Dokument für einen Typ-1-Speicher enthält die folgenden Informationen für Windows-Media Player:</span><span class="sxs-lookup"><span data-stu-id="6dc47-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="6dc47-111">Informationen, die zum Konfigurieren der **Online Store-** Schaltfläche (auch als Registerkarte bezeichnet) verwendet werden, z. b. der Schaltflächen Text, die Schaltflächen Farbe und die QuickInfo für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="6dc47-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="6dc47-112">URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6dc47-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="6dc47-113">URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="6dc47-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="6dc47-114">URL, mit der Windows Media Player das Plug-in des Online Stores abrufen kann, damit das Plug-in auf dem Computer des Benutzers installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6dc47-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="6dc47-115">Wenn Windows Media Player das servicanfo-Dokument aus dem Web abruft, fügt es eine Abfrage Zeichenfolge an die URL an.</span><span class="sxs-lookup"><span data-stu-id="6dc47-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="6dc47-116">Die Abfrage Zeichenfolge enthält Parameter, die Informationen über das Gebiets Schema und den geografischen Standort des Benutzers sowie die Version von Windows Media Player bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6dc47-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dc47-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dc47-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dc47-118">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="6dc47-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6dc47-119">**Dynamisches Erstellen des serviceingefo-Dokuments**</span><span class="sxs-lookup"><span data-stu-id="6dc47-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="6dc47-120">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="6dc47-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="6dc47-121">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="6dc47-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




