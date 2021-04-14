---
description: Die IWebProxy-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: IWebProxy-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393398"
---
# <a name="iwebproxy-properties"></a><span data-ttu-id="92ea5-103">IWebProxy-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92ea5-103">IWebProxy Properties</span></span>

<span data-ttu-id="92ea5-104">Die [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92ea5-104">The [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) interface defines the following properties.</span></span>



| <span data-ttu-id="92ea5-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="92ea5-105">Property</span></span>                                                   | <span data-ttu-id="92ea5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92ea5-106">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92ea5-107">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="92ea5-107">**Address**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | <span data-ttu-id="92ea5-108">Ruft die Adresse und die Dezimal Portnummer des Proxy Servers ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="92ea5-108">Gets and sets the address and the decimal port number of the proxy server.</span></span>                                                |
| [<span data-ttu-id="92ea5-109">**Auto Ermittlung**</span><span class="sxs-lookup"><span data-stu-id="92ea5-109">**AutoDetect**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | <span data-ttu-id="92ea5-110">Ruft einen booleschen Wert ab, der angibt, ob [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) Proxy Einstellungen automatisch erkennt, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="92ea5-110">Gets and sets a Boolean value that indicates whether [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) automatically detects proxy settings.</span></span> |
| [<span data-ttu-id="92ea5-111">**BypassList**</span><span class="sxs-lookup"><span data-stu-id="92ea5-111">**BypassList**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | <span data-ttu-id="92ea5-112">Ruft eine Auflistung von Adressen ab, die den Proxy Server nicht verwenden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="92ea5-112">Gets and sets a collection of addresses that do not use the proxy server.</span></span>                                                 |
| [<span data-ttu-id="92ea5-113">**BypassProxyOnLocal**</span><span class="sxs-lookup"><span data-stu-id="92ea5-113">**BypassProxyOnLocal**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | <span data-ttu-id="92ea5-114">Ruft einen booleschen Wert ab, der angibt, ob lokale Adressen den Proxy Server umgehen, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="92ea5-114">Gets and sets a Boolean value that indicates whether local addresses bypass the proxy server.</span></span>                             |
| [<span data-ttu-id="92ea5-115">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="92ea5-115">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | <span data-ttu-id="92ea5-116">Ruft einen booleschen Wert ab, der angibt, ob das [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) -Objekt schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="92ea5-116">Gets a Boolean value that indicates whether the [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) object is read-only.</span></span>                        |
| [<span data-ttu-id="92ea5-117">**User**</span><span class="sxs-lookup"><span data-stu-id="92ea5-117">**UserName**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | <span data-ttu-id="92ea5-118">Ruft den Benutzernamen ab, der zur Authentifizierung an den Proxy Server gesendet werden soll, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="92ea5-118">Gets and sets the user name to submit to the proxy server for authentication.</span></span>                                             |



 

 

 



