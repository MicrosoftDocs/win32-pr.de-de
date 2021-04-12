---
title: Programmier Handbuch für den Typ 1 Online Stores
description: Programmier Handbuch für den Typ 1 Online Stores
ms.assetid: 6950cab8-4355-4699-8245-f2817c3e25fc
keywords:
- Windows Media Player Online Stores, Programmier Handbuch
- Online Stores, Programmier Handbuch
- Typ 1 Online Stores, Programmier Handbuch
- Programmier Handbuch, Typ 1 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea04cb188a68c85173b5b1682235b6964840d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207169"
---
# <a name="programming-guide-for-type-1-online-stores"></a><span data-ttu-id="2dc31-107">Programmier Handbuch für den Typ 1 Online Stores</span><span class="sxs-lookup"><span data-stu-id="2dc31-107">Programming Guide for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="2dc31-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="2dc31-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2dc31-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dc31-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2dc31-110">Dieser Abschnitt enthält die folgenden Themen, die Ihnen helfen, einen Online Store vom Typ 1 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dc31-110">This section contains the following topics to help you create a type 1 online store.</span></span>



| <span data-ttu-id="2dc31-111">`Section`</span><span class="sxs-lookup"><span data-stu-id="2dc31-111">Section</span></span>                                                                                                              | <span data-ttu-id="2dc31-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dc31-112">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dc31-113">Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1</span><span class="sxs-lookup"><span data-stu-id="2dc31-113">Example ServiceInfo Document for a Type 1 Online Store</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="2dc31-114">Zeigt ein serviceInfo-Beispiel Dokument, das Sie als Ausgangspunkt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2dc31-114">Shows an example ServiceInfo document that you can use as a starting point.</span></span>                                                                    |
| [<span data-ttu-id="2dc31-115">Entwickeln des Plug-Ins für einen Typ-1-Online Shop</span><span class="sxs-lookup"><span data-stu-id="2dc31-115">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)                 | <span data-ttu-id="2dc31-116">Erläutert, wie das erforderliche Plug-in für einen Typ-1-Online Shop erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2dc31-116">Explains how to build the required plug-in for a type 1 online store.</span></span>                                                                          |
| [<span data-ttu-id="2dc31-117">Anzeigen von Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="2dc31-117">Displaying Dialog Boxes</span></span>](displaying-dialog-boxes.md)                                                               | <span data-ttu-id="2dc31-118">Erläutert das Aufrufen von Dialogfeldern über Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2dc31-118">Explains how to invoke dialog boxes through Windows Media Player.</span></span>                                                                              |
| [<span data-ttu-id="2dc31-119">Verwalten der Anmeldung</span><span class="sxs-lookup"><span data-stu-id="2dc31-119">Managing Login</span></span>](managing-login.md)                                                                                 | <span data-ttu-id="2dc31-120">Erläutert die Interaktion mit Windows-Media Player Benutzeroberflächen Elementen, mit denen Benutzer sich bei dem Online Shop anmelden und sich abmelden können.</span><span class="sxs-lookup"><span data-stu-id="2dc31-120">Explains how to interact with Windows Media Player user interface elements that let users log in to and log out from the online store.</span></span>         |
| [<span data-ttu-id="2dc31-121">Erwerben von Medieninhalten</span><span class="sxs-lookup"><span data-stu-id="2dc31-121">Purchasing Media Content</span></span>](purchasing-media-content.md)                                                             | <span data-ttu-id="2dc31-122">Erläutert, wie Windows Media Player und das Plug-in des Online Stores interagieren, wenn der Benutzer Medieninhalte erwirbt.</span><span class="sxs-lookup"><span data-stu-id="2dc31-122">Explains how Windows Media Player and the online store's plug-in interact when the user purchases media content.</span></span>                               |
| [<span data-ttu-id="2dc31-123">Herunterladen von Medieninhalten</span><span class="sxs-lookup"><span data-stu-id="2dc31-123">Downloading Media Content</span></span>](downloading-media-content.md)                                                           | <span data-ttu-id="2dc31-124">Erläutert, wie Windows Media Player und das Plug-in des Online Stores interagieren, wenn der Benutzer Medieninhalte herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="2dc31-124">Explains how Windows Media Player and the online store's plug-in interact when the user downloads media content.</span></span>                               |
| [<span data-ttu-id="2dc31-125">Aktualisieren von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="2dc31-125">Updating Licenses</span></span>](updating-licenses.md)                                                                           | <span data-ttu-id="2dc31-126">Erläutert, wie Windows Media Player und das Plug-in des Online Stores interagieren, um die Medien Lizenzen des Benutzers auf dem neuesten Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="2dc31-126">Explains how Windows Media Player and the online store's plug-in interact to keep the user's media licenses current.</span></span>                           |
| [<span data-ttu-id="2dc31-127">Aktualisieren von tragbaren Geräten</span><span class="sxs-lookup"><span data-stu-id="2dc31-127">Updating Portable Devices</span></span>](updating-portable-devices.md)                                                           | <span data-ttu-id="2dc31-128">Erläutert, wie Windows Media Player und das Plug-in des Online Stores interagieren, wenn Medieninhalte zwischen dem Computer und einem tragbaren Gerät verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="2dc31-128">Explains how Windows Media Player and the online store's plug-in interact when media content moves between the computer and a portable device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2dc31-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2dc31-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dc31-130">**Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="2dc31-130">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




