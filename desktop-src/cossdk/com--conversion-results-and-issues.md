---
description: Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in com+-Anwendungen konvertieren oder Sie vom Microsoft Windows Setup-Prozess automatisch ausführen lassen, sollten Sie sich über die Ergebnisse der Konvertierung und die Probleme informieren.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Ergebnisse und Probleme bei der com+-Konvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393234"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="44ff5-103">Ergebnisse und Probleme bei der com+-Konvertierung</span><span class="sxs-lookup"><span data-stu-id="44ff5-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="44ff5-104">Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in com+-Anwendungen konvertieren oder Sie vom Microsoft Windows Setup-Prozess automatisch ausführen lassen, sollten Sie sich über die Ergebnisse der Konvertierung und die Probleme informieren.</span><span class="sxs-lookup"><span data-stu-id="44ff5-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="44ff5-105">Was konvertiert wird</span><span class="sxs-lookup"><span data-stu-id="44ff5-105">What Is Converted</span></span>

<span data-ttu-id="44ff5-106">Während der Konvertierung konvertiert das Dienstprogramm mtstocom Rollen, Rollenzuweisungen, Schnittstellen, Methoden, Benutzer, die Computer Liste und die meisten Computereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="44ff5-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="44ff5-107">Das Dienstprogramm mtstocom konvertiert außerdem die Identität und das Kennwort für ein MTS-Paket.</span><span class="sxs-lookup"><span data-stu-id="44ff5-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="44ff5-108">Die neuen com+-Attribute, die in MTS nicht verfügbar waren, werden automatisch auf die folgenden Standardwerte für alle konvertierten MTS-Komponenten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44ff5-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="44ff5-109">Diese Standardeinstellungen können entweder mit dem Verwaltungs Programmkomponenten Dienste oder mit den administrativen Verwaltungs Schnittstellen von com+ geändert werden.</span><span class="sxs-lookup"><span data-stu-id="44ff5-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="44ff5-110">Die JIT-Aktivierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="44ff5-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="44ff5-111">Objekt Pooling deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="44ff5-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="44ff5-112">Synchronisierung identisch mit der Transaktions Einstellung.</span><span class="sxs-lookup"><span data-stu-id="44ff5-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="44ff5-113">Konvertierungsprobleme</span><span class="sxs-lookup"><span data-stu-id="44ff5-113">Conversion Issues</span></span>

<span data-ttu-id="44ff5-114">Com+ wird automatisch installiert, wenn Sie Windows installieren.</span><span class="sxs-lookup"><span data-stu-id="44ff5-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="44ff5-115">Es ist nicht möglich, com+ zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="44ff5-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="44ff5-116">Probleme im Zusammenhang mit Upgrades vorhandener MTS-und com+-Installationen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="44ff5-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="44ff5-117">Wenn Sie zurzeit MTS 1,0 verwenden, wird MTS automatisch auf com+ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ff5-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="44ff5-118">Benutzerdefinierte Pakete gehen jedoch verloren und müssen neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44ff5-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="44ff5-119">Wenn Sie zurzeit MTS 2,0 verwenden, wird MTS automatisch auf com+ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ff5-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="44ff5-120">Alle benutzerdefinierten Pakete werden auf COM+-Anwendungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ff5-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="44ff5-121">Alle Komponenten sollten wie unter MTS 2,0 funktionieren.</span><span class="sxs-lookup"><span data-stu-id="44ff5-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="44ff5-122">Wenn Sie die Optionen MTS 1,0 und MTS 2,0 verwenden und die SDK-Option installiert haben, werden die SDK-Dateien entfernt.</span><span class="sxs-lookup"><span data-stu-id="44ff5-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="44ff5-123">Sie können das aktuelle com+-SDK über die Microsoft Windows SDK installieren.</span><span class="sxs-lookup"><span data-stu-id="44ff5-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="44ff5-124">Sie können einen Remote Computer mit dem Computer nicht von einem com+-Computer aus verwalten.</span><span class="sxs-lookup"><span data-stu-id="44ff5-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44ff5-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44ff5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ff5-126">Automatische Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="44ff5-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="44ff5-127">Manuelle Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="44ff5-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="44ff5-128">MTS-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44ff5-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



