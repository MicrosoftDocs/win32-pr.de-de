---
description: Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit-Windows Installer Komponenten.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64-Bit-Windows Installer Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864540"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="4a2ce-103">64-Bit-Windows Installer Pakete</span><span class="sxs-lookup"><span data-stu-id="4a2ce-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="4a2ce-104">Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit- [Windows Installer](windows-installer-components.md) Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="4a2ce-105">In der folgenden Liste sind die Anforderungen für alle 64-Bit-Windows Installer Pakets aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="4a2ce-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="4a2ce-106">Der Wert "Intel64" muss im Feld Platform der [**Template Summary**](template-summary.md) -Eigenschaft nur dann eingegeben werden, wenn das Paket auf einem Intel64-Prozessor (Itanium) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="4a2ce-107">Der Wert "x64" muss in das Feld "Platform" der [**Template Summary**](template-summary.md) -Eigenschaft eingegeben werden, wenn das Paket auf einem x64-Prozessor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="4a2ce-108">Der Wert "Arm64" muss in das Feld Platform der [**Template Summary**](template-summary.md) -Eigenschaft eingegeben werden, wenn das Paket auf einem Arm64-Prozessor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="4a2ce-109">Die [**Seitenanzahl-Zusammenfassungs**](page-count-summary.md) Eigenschaft muss auf die ganze Zahl 200 oder höher festgelegt werden, da Windows Installer 2,0 die Mindestversion ist, die die Installation von 64-Bit-Komponenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="4a2ce-110">Für Pakete für die Arm64-Plattform ist der Wert 500 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="4a2ce-111">Jede 64-Bit-Windows Installer Komponente im Paket muss das **msidbComponentAttributes64bit** -Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="4a2ce-112">Weitere Informationen finden Sie unter [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) und [32-Bit-Windows Installer Paketen](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="4a2ce-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



