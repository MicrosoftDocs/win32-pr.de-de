---
description: Die iupdateingestaller-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Iupdateingestaller-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862795"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="409e9-103">Iupdateingestaller-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="409e9-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="409e9-104">Die [**iupdateingestaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="409e9-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="409e9-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="409e9-105">Property</span></span>                                                                                      | <span data-ttu-id="409e9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="409e9-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="409e9-107">**Allowsourceaufforderungen**</span><span class="sxs-lookup"><span data-stu-id="409e9-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="409e9-108">Ruft einen booleschen Wert ab, der angibt, ob beim Installieren der Updates Quell Aufforderungen für den Benutzer angezeigt werden sollen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="409e9-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="409e9-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="409e9-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="409e9-110">Ruft die aktuelle Client Anwendung ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="409e9-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="409e9-111">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="409e9-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="409e9-112">Ruft einen booleschen Wert ab, der angibt, ob auf einem Computer zu einem bestimmten Zeitpunkt eine Installation oder eine Deinstallation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="409e9-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="409e9-113">**Isforced**</span><span class="sxs-lookup"><span data-stu-id="409e9-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="409e9-114">Ruft einen booleschen Wert ab, der angibt, ob ein Update zwangsweise installiert oder deinstalliert wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="409e9-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="409e9-115">**Klammer**</span><span class="sxs-lookup"><span data-stu-id="409e9-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="409e9-116">Ruft ein Handle für das übergeordnete Fenster ab, das ein Dialogfeld enthalten kann, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="409e9-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="409e9-117">**Fenster Fenster**</span><span class="sxs-lookup"><span data-stu-id="409e9-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="409e9-118">Dient zum Abrufen und Festlegen der-Schnittstelle, die das übergeordnete Fenster darstellt, das ein Dialogfeld enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="409e9-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="409e9-119">**Rebootrequiredbeforeingestallations**</span><span class="sxs-lookup"><span data-stu-id="409e9-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="409e9-120">Ruft einen booleschen Wert ab, der angibt, ob vor dem Installieren oder Deinstallieren von Updates ein Systemneustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="409e9-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="409e9-121">**Updates**</span><span class="sxs-lookup"><span data-stu-id="409e9-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="409e9-122">Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der für die Installation oder die Installation angegebenen Updates enthält, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="409e9-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



