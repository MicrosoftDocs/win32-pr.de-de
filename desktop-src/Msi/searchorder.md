---
description: Durch Festlegen dieser pro-Benutzer-System Richtlinie wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869047"
---
# <a name="searchorder"></a><span data-ttu-id="d8250-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="d8250-103">SearchOrder</span></span>

<span data-ttu-id="d8250-104">Durch Festlegen dieser pro-Benutzer- [System Richtlinie](system-policy.md) wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht.</span><span class="sxs-lookup"><span data-stu-id="d8250-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="d8250-105">Die Typen der Quellen sind:</span><span class="sxs-lookup"><span data-stu-id="d8250-105">The types of sources are:</span></span>

<span data-ttu-id="d8250-106">"n" – Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d8250-106">"n" – network</span></span>

<span data-ttu-id="d8250-107">"m" – Medium (CD-ROM oder DVD)</span><span class="sxs-lookup"><span data-stu-id="d8250-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="d8250-108">"u" – Uniform Resource Locator (URL)</span><span class="sxs-lookup"><span data-stu-id="d8250-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="d8250-109">Wenn Sie z. b. zuerst nach Netzwerk Quellen suchen möchten, legen die Medienquellen und die URL-Quellen zuletzt diese Richtlinie auf den Wert "NMU" fest.</span><span class="sxs-lookup"><span data-stu-id="d8250-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="d8250-110">Wenn Sie die Suche nach einem bestimmten Quelltyp weglassen möchten, lassen Sie den entsprechenden Buchstaben aus dem Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8250-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="d8250-111">Wenn SearchOrder nicht festgelegt ist, lautet die Standard Such Reihenfolge Network, Media und then URL.</span><span class="sxs-lookup"><span data-stu-id="d8250-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="d8250-112">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d8250-112">Registry Key</span></span>

<span data-ttu-id="d8250-113">**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d8250-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d8250-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d8250-114">Data Type</span></span>

<span data-ttu-id="d8250-115">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="d8250-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8250-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8250-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8250-117">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="d8250-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



