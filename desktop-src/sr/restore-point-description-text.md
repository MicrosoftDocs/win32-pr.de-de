---
title: Wiederherstellungspunkt-Beschreibungs Text
description: Wenn eine Anwendung die SRSetRestorePoint-Funktion aufruft, kann Sie beliebigen Text als Beschreibung für den Wiederherstellungspunkt angeben. in der folgenden Tabelle wird jedoch der empfohlene Beschreibungstext angezeigt.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206861"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="56c16-103">Wiederherstellungspunkt-Beschreibungs Text</span><span class="sxs-lookup"><span data-stu-id="56c16-103">Restore Point Description Text</span></span>

<span data-ttu-id="56c16-104">Wenn eine Anwendung die [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) -Funktion aufruft, kann Sie beliebigen Text als Beschreibung für den Wiederherstellungspunkt angeben. in der folgenden Tabelle wird jedoch der empfohlene Beschreibungstext angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56c16-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="56c16-105">System Änderung</span><span class="sxs-lookup"><span data-stu-id="56c16-105">System modification</span></span>                            | <span data-ttu-id="56c16-106">Typ des Wiederherstellungs Punkts</span><span class="sxs-lookup"><span data-stu-id="56c16-106">Restore point type</span></span>      | <span data-ttu-id="56c16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56c16-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="56c16-108">Anwendungsinstallation</span><span class="sxs-lookup"><span data-stu-id="56c16-108">Application installation</span></span>                       | <span data-ttu-id="56c16-109">Anwendungs \_ Installation</span><span class="sxs-lookup"><span data-stu-id="56c16-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="56c16-110">Installierter *appname*</span><span class="sxs-lookup"><span data-stu-id="56c16-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="56c16-111">Anwendungs Änderung (Features hinzufügen/entfernen)</span><span class="sxs-lookup"><span data-stu-id="56c16-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="56c16-112">\_Einstellungen ändern</span><span class="sxs-lookup"><span data-stu-id="56c16-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="56c16-113">Konfigurierter *appname*</span><span class="sxs-lookup"><span data-stu-id="56c16-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="56c16-114">Entfernen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="56c16-114">Application removal</span></span>                            | <span data-ttu-id="56c16-115">Anwendungs \_ Deinstallation</span><span class="sxs-lookup"><span data-stu-id="56c16-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="56c16-116">*Appname* wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="56c16-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="56c16-117">Gerätetreiber Installation</span><span class="sxs-lookup"><span data-stu-id="56c16-117">Device driver installation</span></span>                     | <span data-ttu-id="56c16-118">Geräte \_ Treiber \_ Installation</span><span class="sxs-lookup"><span data-stu-id="56c16-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="56c16-119">Installierter *DriverName*</span><span class="sxs-lookup"><span data-stu-id="56c16-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="56c16-120">Installationsprogramme, z. b. Windows Installer und InstallShield, verwenden diese Konventionen für den Beschreibungstext:</span><span class="sxs-lookup"><span data-stu-id="56c16-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="56c16-121">Der Produktname folgt dem Verb. Beispiel: installierter *appname*.</span><span class="sxs-lookup"><span data-stu-id="56c16-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="56c16-122">Der Produktname kann allein (*appname*) oder der Produktname verwendet werden, und der Name des Unternehmens kann jeweils verwendet werden (*MyCompany appname*).</span><span class="sxs-lookup"><span data-stu-id="56c16-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




