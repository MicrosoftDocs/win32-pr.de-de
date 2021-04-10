---
title: Festlegen des ersten Online Stores
description: Festlegen des ersten Online Stores
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Windows Media Player Online Stores, Festlegen von anfänglichen Online Stores
- Online Stores, Festlegen von anfänglichen Online Stores
- Geben Sie 1 Online Stores ein, und legen Sie anfängliche Online Stores fest
- Geben Sie 2 Online Stores ein, und legen Sie anfängliche Online Stores fest
- Windows Media Player Online Stores, erster Online Shop angezeigt
- Online Stores, erster Online Shop angezeigt
- Typ 1 Online Stores, erster Online Shop angezeigt
- Typ 2 Online Stores, erster Online Shop angezeigt
- der erste Online Shop wird angezeigt.
- Festlegen der anfänglichen Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856592"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="79e9f-113">Festlegen des ersten Online Stores</span><span class="sxs-lookup"><span data-stu-id="79e9f-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="79e9f-114">Ausführliche Informationen zur Neuverteilung von Windows Media Player-Software mit Ihrer Anwendung finden Sie unter [Verteilen von Windows Media Player Software](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="79e9f-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="79e9f-115">Wenn ein Benutzer zunächst Windows Media Player installiert, legt die Setup Anwendung den ersten aktiven Online Store auf einen von Microsoft ausgewählten Standard fest.</span><span class="sxs-lookup"><span data-stu-id="79e9f-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="79e9f-116">Die Originalgerätehersteller (OEMs) für persönliche Computer können diese Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="79e9f-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="79e9f-117">Zum angeben und Konfigurieren des ersten Online Stores, der dem Benutzer angezeigt wird, wenn er Windows Media Player installiert, müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="79e9f-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="79e9f-118">Erstellen Sie ein servicinput Info-Dokument, das Sie auf der Festplatte des Benutzers installieren.</span><span class="sxs-lookup"><span data-stu-id="79e9f-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="79e9f-119">Dieses Dokument enthält Informationen zum Konfigurieren des ersten aktiven Online Stores.</span><span class="sxs-lookup"><span data-stu-id="79e9f-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="79e9f-120">Fügen Sie beim Ausführen der Setup Anwendung eine Reihe von Befehlszeilen Parametern an.</span><span class="sxs-lookup"><span data-stu-id="79e9f-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="79e9f-121">Es gibt drei Szenarien für die Installation von Windows Media Player und das Festlegen des ersten Online Stores.</span><span class="sxs-lookup"><span data-stu-id="79e9f-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="79e9f-122">In den folgenden Abschnitten finden Sie weitere Informationen zu den einzelnen Szenarien:</span><span class="sxs-lookup"><span data-stu-id="79e9f-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="79e9f-123">Offline Installation</span><span class="sxs-lookup"><span data-stu-id="79e9f-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="79e9f-124">Installation von einer CD während der Online Installation</span><span class="sxs-lookup"><span data-stu-id="79e9f-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="79e9f-125">Installation über das Web während der Online Installation</span><span class="sxs-lookup"><span data-stu-id="79e9f-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="79e9f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79e9f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e9f-127">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="79e9f-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="79e9f-128">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="79e9f-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="79e9f-129">**Einrichten von Befehlszeilen Parametern für Online Stores**</span><span class="sxs-lookup"><span data-stu-id="79e9f-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




