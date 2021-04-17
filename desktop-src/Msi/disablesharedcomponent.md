---
description: Wenn diese pro-Computer-System Richtlinie auf 1 festgelegt ist, ruft kein Paket auf dem System die Funktionalität der freigegebenen Komponente ab, die durch das msidbcomponentattributesshared-Attribut in der Component-Tabelle aktiviert wird.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: Disablesharedcomponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527038"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="30e11-103">Disablesharedcomponent</span><span class="sxs-lookup"><span data-stu-id="30e11-103">DisableSharedComponent</span></span>

<span data-ttu-id="30e11-104">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf 1 festgelegt ist, ruft kein Paket auf dem System die Funktionalität der freigegebenen Komponente ab, die durch das **msidbcomponentattributesshared** -Attribut in der [Component-Tabelle](component-table.md)aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="30e11-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="30e11-105">Der Standardwert ist 0 (null). Dadurch wird die Funktionalität der freigegebenen Komponente für Komponenten aktiviert, die mit **msidbcomponentattributesshared** in allen Paketen gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="30e11-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="30e11-106">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30e11-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="30e11-107">Diese Funktion ist ab Windows Installer 4,5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30e11-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="30e11-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="30e11-108">Registry Key</span></span>

<span data-ttu-id="30e11-109">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="30e11-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="30e11-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="30e11-110">Data Type</span></span>

<span data-ttu-id="30e11-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="30e11-111">**REG\_DWORD**</span></span>

 

 



