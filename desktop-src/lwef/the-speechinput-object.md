---
title: Das speechinput-Objekt
description: Das speechinput-Objekt
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947870"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="6d0eb-103">Das speechinput-Objekt</span><span class="sxs-lookup"><span data-stu-id="6d0eb-103">The SpeechInput Object</span></span>

<span data-ttu-id="6d0eb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6d0eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6d0eb-105">Das [**speechinput**](https://www.bing.com/search?q=**SpeechInput**) -Objekt ermöglicht den Zugriff auf die Spracheingabe Eigenschaften, die vom Agent-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="6d0eb-106">Die Eigenschaften sind für Client Anwendungen schreibgeschützt, aber der Benutzer kann Sie auf der Eigenschaften Seite des Microsoft-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="6d0eb-107">Der Server gibt nur dann Werte zurück, wenn eine kompatible Sprach-Engine installiert und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="6d0eb-108">Die Eigenschaften [**Engine**](https://www.bing.com/search?q=**Engine**), [**installiert**](https://www.bing.com/search?q=**Installed**)und [**Language**](https://www.bing.com/search?q=**Language**) werden nicht mehr unterstützt, aber (aus Gründen der Abwärtskompatibilität) geben NULL-Werte zurück, wenn Sie abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="6d0eb-109">Um den Modus einer Spracherkennung abzufragen oder festzulegen, verwenden Sie die [**srmodeid**](srmodeid-property.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="6d0eb-110">Speechinput-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d0eb-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




