---
title: Iagentspeechinputproperties
description: Iagentspeechinputproperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387931"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="96c1c-103">Iagentspeechinputproperties</span><span class="sxs-lookup"><span data-stu-id="96c1c-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="96c1c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="96c1c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="96c1c-105">Iagentspeechinputproperties ermöglicht den Zugriff auf die Spracheingabe Eigenschaften, die vom Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="96c1c-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="96c1c-106">Die meisten Eigenschaften sind für Client Anwendungen schreibgeschützt, aber der Benutzer kann Sie auf der Eigenschaften Seite des Microsoft-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="96c1c-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="96c1c-107">Der Microsoft-Agent-Server gibt Werte nur dann zurück, wenn eine kompatible Sprach-Engine installiert und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="96c1c-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="96c1c-108">Wenn Sie diese Eigenschaften Abfragen, wird versucht, die Sprach-Engine zu starten.</span><span class="sxs-lookup"><span data-stu-id="96c1c-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="96c1c-109">**Methoden in Vtable-Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="96c1c-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="96c1c-110">Iagentspeechinputproperties-Methoden</span><span class="sxs-lookup"><span data-stu-id="96c1c-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="96c1c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96c1c-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="96c1c-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="96c1c-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="96c1c-113">Gibt zurück, ob die Spracherkennungs-Engine aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="96c1c-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="96c1c-114">**GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="96c1c-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="96c1c-115">Gibt die aktuelle Schlüsselzuweisung des Abhör Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="96c1c-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="96c1c-116">**Getlisteningtip**</span><span class="sxs-lookup"><span data-stu-id="96c1c-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="96c1c-117">Gibt zurück, ob der Abhör Tipp aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="96c1c-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="96c1c-118">Die Methoden [**getinstallierte**](https://www.bing.com/search?q=**GetInstalled**), [**GetLcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)und [**ltengine**](https://www.bing.com/search?q=**SetEngine**) (in früheren Versionen des Microsoft-Agents unterstützt) werden weiterhin aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="96c1c-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="96c1c-119">Allerdings werden die Methoden nicht als Stub und keine nützlichen Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96c1c-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="96c1c-120">Verwenden Sie [**getsrmodeid**](https://www.bing.com/search?q=**GetSRModeID**) und [**setsrmodeid**](https://www.bing.com/search?q=**SetSRModeID**) , um die Spracherkennungs-Engine abzufragen und festzulegen, die mit dem Zeichen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96c1c-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="96c1c-121">Beachten Sie, dass die Engine die aktuelle Spracheinstellung des Zeichens entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="96c1c-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




