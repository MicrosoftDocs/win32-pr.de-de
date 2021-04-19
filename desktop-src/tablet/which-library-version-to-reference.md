---
description: In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Welche Bibliotheks Version soll referenziert werden?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346933"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="1754d-103">Welche Bibliotheks Version soll referenziert werden?</span><span class="sxs-lookup"><span data-stu-id="1754d-103">Which Library Version to Reference</span></span>

<span data-ttu-id="1754d-104">In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1754d-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="1754d-105">Tablet PC-Bibliotheksversionen</span><span class="sxs-lookup"><span data-stu-id="1754d-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="1754d-106">Die Binärdateien der Tablet PC-Bibliothek (Microsoft.Ink.dll) wurden in Windows Vista aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1754d-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="1754d-107">Diese Binärdateien werden als "Version 6,0" bezeichnet, um zusammen mit der Windows-Version, in der Sie veröffentlicht werden, eine Zusammenfassung zu finden.</span><span class="sxs-lookup"><span data-stu-id="1754d-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="1754d-108">Die neueste Version der Binärdateien, die mit Windows XP kompatibel sind, wird als "Version 1,7" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1754d-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="1754d-109">Der Windows SDK kann sowohl auf Vista-als auch auf XP-Computern installiert werden, und die Windows SDK umfasst beide Versionen von Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="1754d-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="1754d-110">Diese werden in installiert:</span><span class="sxs-lookup"><span data-stu-id="1754d-110">These are installed in:</span></span>

1. <span data-ttu-id="1754d-111">% Program Files% \\ Verweisassemblys \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="1754d-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="1754d-112">% Program Files% \\ Verweisassemblys \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="1754d-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="1754d-113">Die Binärdateien der Version 6,0 sind nur mit Windows Vista kompatibel, und Anwendungen, die für diese geschrieben wurden, sollten nur unter Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1754d-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="1754d-114">Eine Anwendung, die für die Binärdateien der Version 1,7 geschrieben wurde, sollte unverändert bei der Installation unter Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1754d-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



