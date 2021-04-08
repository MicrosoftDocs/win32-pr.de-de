---
description: Das callhub-Objekt macht Methoden verfügbar, mit denen Informationen zu Teilnehmern in einem Aufruf von mehreren Parteien abgerufen werden.
ms.assetid: 928c3abb-1b4e-42f3-a8cc-41889ad573ed
title: Callhub-Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe448c7f559d38bef671144c1a6457f43d4a6b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866591"
---
# <a name="callhub-object-interfaces"></a><span data-ttu-id="8412c-103">Callhub-Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8412c-103">CallHub Object Interfaces</span></span>

<span data-ttu-id="8412c-104">Das [callhub-Objekt](callhub-object.md) macht Methoden verfügbar, mit denen Informationen zu Teilnehmern in einem Aufruf von mehreren Parteien abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8412c-104">The [CallHub object](callhub-object.md) exposes methods that retrieve information concerning participants in a multi-party call.</span></span>

<span data-ttu-id="8412c-105">Die [**itcallhubevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) -und [**ienumcallhub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) -Schnittstellen werden nicht direkt für das callhub-Objekt verfügbar gemacht, sind aber eng damit verknüpft und werden hier zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="8412c-105">The [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) and [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) interfaces are not directly exposed on the CallHub Object, but are tightly related to it and are listed here for reference convenience.</span></span>



| <span data-ttu-id="8412c-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8412c-106">Interface</span></span>                                | <span data-ttu-id="8412c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8412c-107">Description</span></span>                                                           |
|------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8412c-108">**Itcallhub**</span><span class="sxs-lookup"><span data-stu-id="8412c-108">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)           | <span data-ttu-id="8412c-109">Stellt Methoden zum Abrufen von Informationen zu einem callhub-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="8412c-109">Provides methods to retrieve information concerning a CallHub object.</span></span> |
| [<span data-ttu-id="8412c-110">**Itcallhubevent**</span><span class="sxs-lookup"><span data-stu-id="8412c-110">**ITCallHubEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) | <span data-ttu-id="8412c-111">Wird zum Abrufen von Informationen zu callhub-Ereignissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8412c-111">Used to acquire information concerning CallHub events.</span></span>                |
| [<span data-ttu-id="8412c-112">**Ienumcallhub**</span><span class="sxs-lookup"><span data-stu-id="8412c-112">**IEnumCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)     | <span data-ttu-id="8412c-113">Listet [**itcallhub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)auf.</span><span class="sxs-lookup"><span data-stu-id="8412c-113">Enumerates [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span></span>                            |



 

 

 



