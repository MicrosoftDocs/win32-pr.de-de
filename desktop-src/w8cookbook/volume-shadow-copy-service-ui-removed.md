---
title: Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.
description: Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474485"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="a36a1-103">Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.</span><span class="sxs-lookup"><span data-stu-id="a36a1-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="a36a1-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="a36a1-104">Platform</span></span>

<span data-ttu-id="a36a1-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="a36a1-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="a36a1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a36a1-106">Description</span></span>

<span data-ttu-id="a36a1-107">In früheren Versionen von Windows konnten Benutzer vorherige Versionen einzelner Dateien aus "Schatten Kopien" von lokalen Volumes wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="a36a1-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="a36a1-108">Diese Schatten Kopien werden mithilfe des Volumeschattenkopie-Diensts (VSS) durch das Feature "vorherige Versionen" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a36a1-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="a36a1-109">In Windows 7 konnten Benutzer Schatten Kopien in der Benutzeroberfläche des System Schutzes konfigurieren und planen, die über Systemeigenschaften verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a36a1-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="a36a1-110">Frühere Versionen wurden jedoch selten verwendet und beeinflussen die gesamte Windows-Leistung. Daher wurde die Funktion entfernt.</span><span class="sxs-lookup"><span data-stu-id="a36a1-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="a36a1-111">In Windows 8 sind diese Features nicht mehr verfügbar:</span><span class="sxs-lookup"><span data-stu-id="a36a1-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="a36a1-112">Die Möglichkeit zum Durchsuchen, durchsuchen oder Wiederherstellen früherer Dateiversionen über die Benutzeroberfläche der vorherigen Versionen</span><span class="sxs-lookup"><span data-stu-id="a36a1-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="a36a1-113">Die Möglichkeit, frühere Versionen von Dateien über die Benutzeroberfläche des System Schutzes zu konfigurieren oder zu planen</span><span class="sxs-lookup"><span data-stu-id="a36a1-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="a36a1-114">Benutzer können jedoch weiterhin die Registerkarte Vorherige Versionen verwenden, wenn Sie auf Dateifreigaben auf einem Windows-Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a36a1-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a36a1-115">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="a36a1-115">Manifestation</span></span>

<span data-ttu-id="a36a1-116">Die Option "vorherige Versionen" ist nicht mehr für lokale Volumes im Eigenschaften Menü von Windows Explorer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a36a1-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="a36a1-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="a36a1-117">Solution</span></span>

<span data-ttu-id="a36a1-118">Entwickler, die Schatten Kopien von lokalen Volumes erstellen müssen, können dies weiterhin tun, indem Sie VSS-APIs in benutzerdefiniertem Code aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a36a1-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




