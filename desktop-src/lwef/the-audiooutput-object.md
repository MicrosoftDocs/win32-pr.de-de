---
title: Das Audiooutput-Objekt
description: Das Audiooutput-Objekt
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390313"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="4208c-103">Das Audiooutput-Objekt</span><span class="sxs-lookup"><span data-stu-id="4208c-103">The AudioOutput Object</span></span>

<span data-ttu-id="4208c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4208c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4208c-105">Dieses Objekt ermöglicht den Zugriff auf audioausgabeeigenschaften, die vom Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4208c-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="4208c-106">Die Eigenschaften sind schreibgeschützt, aber der Benutzer kann Sie im Eigenschaften Blatt Microsoft-Agent ändern.</span><span class="sxs-lookup"><span data-stu-id="4208c-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="4208c-107">Wenn Sie eine Objekt Variable des Typs [**iagentctlaudioobjectex**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)deklarieren, können Sie nicht auf alle Eigenschaften für das [**Audiooutput**](/windows/desktop/lwef/the-audiooutput-object) -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4208c-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="4208c-108">Obwohl der-Agent auch [**iagentctlaudioobject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)unterstützt, wird diese letztere Schnittstelle nur aus Gründen der Abwärtskompatibilität bereitgestellt und unterstützt nur diese Eigenschaften in früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="4208c-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="4208c-109">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="4208c-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="4208c-110">**Sounentffects**</span><span class="sxs-lookup"><span data-stu-id="4208c-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="4208c-111">**Status**</span><span class="sxs-lookup"><span data-stu-id="4208c-111">**Status**</span></span>](status-property.md)

 

 