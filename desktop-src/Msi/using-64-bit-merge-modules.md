---
description: Befolgen Sie diese Richtlinien, wenn Sie ein 64-Bit-Mergemodul erstellen.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Verwenden von 64-Bit-Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757806"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="664a7-103">Verwenden von 64-Bit-Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="664a7-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="664a7-104">Ein 64-Bit-Mergemodul hat eine der in diesem Thema identifizierten Merkmale.</span><span class="sxs-lookup"><span data-stu-id="664a7-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="664a7-105">Das Mergemodul enthält mindestens eine Komponente, die für 64-Bit-Betriebssysteme kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="664a7-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="664a7-106">Das Mergemodul enthält keine 64-Bit-Komponenten, sondern ist nur für die Verwendung mit [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paketen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="664a7-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="664a7-107">Mergemodule können wie folgt verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="664a7-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="664a7-108">Ein 64-Bit-Mergemodul kann in ein [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paket zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="664a7-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="664a7-109">Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaften im Mergemodul und im Windows Installer Paket müssen auf denselben Typ von 64-Bit-Prozessor festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="664a7-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="664a7-110">Ein x64-Mergemodul kann nur in x64-Paketen zusammengeführt werden, und ein Intel64 Merge-Modul kann nur in Intel64-Paketen zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="664a7-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="664a7-111">Ein 32-Bit-Mergemodul kann mit 32-Bit-oder [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paketen zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="664a7-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="664a7-112">Ein 64-Bit-Mergemodul kann in einem 64-Bit-Paket unter einem 32-Bit-Betriebssystem zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="664a7-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="664a7-113">Beachten Sie beim Erstellen eines 64-Bit-Mergemoduls Folgendes:</span><span class="sxs-lookup"><span data-stu-id="664a7-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="664a7-114">Verwenden Sie das gleiche allgemeine Verfahren wie beim Erstellen von 32-Bit-Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="664a7-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="664a7-115">Weitere Informationen finden Sie unter Informationen [zu Mergemodulen](about-merge-modules.md) und zum [Erstellen von Mergemodulen](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="664a7-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="664a7-116">Wenn ein Intel64-System ausgeführt wird, müssen Sie die Eigenschaft [**Vorlagen Zusammenfassung**](template-summary.md) mit dem Wert Intel64 festlegen.</span><span class="sxs-lookup"><span data-stu-id="664a7-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="664a7-117">Wenn Sie ein x64-System ausführen, müssen Sie die Eigenschaft **Vorlagen Zusammenfassung** mit dem x64-Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="664a7-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="664a7-118">Weitere Informationen finden Sie unter [Zusammenfassungs Datenstrom Referenz für Zusammenfassungs Modul](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="664a7-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="664a7-119">Wenn sowohl 32-Bit-als auch 64-Bit-Mergemodule für dieselbe Komponente vorhanden sind, wird empfohlen, dass die Module unterschiedliche Signaturen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="664a7-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="664a7-120">Dadurch kann ein Paket beide Versionen der Komponente enthalten.</span><span class="sxs-lookup"><span data-stu-id="664a7-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="664a7-121">Weitere Informationen finden Sie unter [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="664a7-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



