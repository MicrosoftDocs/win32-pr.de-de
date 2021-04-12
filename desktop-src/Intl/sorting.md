---
description: Für NLS wird die Sortierung (auch als &\# 0034; COLLATIONS&\# 0034;) bezeichnet. die Anordnung von Zeichen folgen.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Sortierung (Internationalisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218545"
---
# <a name="sorting"></a><span data-ttu-id="4564e-103">Sortierung</span><span class="sxs-lookup"><span data-stu-id="4564e-103">Sorting</span></span>

<span data-ttu-id="4564e-104">Bei nls ist das Sortieren (auch als "Sortierung" bezeichnet) die Anordnung von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="4564e-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="4564e-105">Es gibt zwei Arten der Sortierung:</span><span class="sxs-lookup"><span data-stu-id="4564e-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="4564e-106">Linguistische Sortierung.</span><span class="sxs-lookup"><span data-stu-id="4564e-106">Linguistic sorting.</span></span> <span data-ttu-id="4564e-107">Ordnet Zeichen folgen mit ähnlichen linguistischen Merkmalen in Gruppen (sortiert) an.</span><span class="sxs-lookup"><span data-stu-id="4564e-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="4564e-108">Ordnungszahl (nicht linguistisch).</span><span class="sxs-lookup"><span data-stu-id="4564e-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="4564e-109">Ordnet die Zeichen folgen in einer geordneten Sequenz an.</span><span class="sxs-lookup"><span data-stu-id="4564e-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="4564e-110">Die Sortierung verwendet die NLS-Zeichen folgen Vergleichsfunktionen, wie z. b. [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), oder Wrapper-API-Funktionen, wie z. b. [lstraucmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), die intern die NLS-Zeichen folgen Vergleichsfunktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4564e-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="4564e-111">Ausführliche Informationen zum Implementieren von Sortierungen in Ihren Anwendungen finden Sie unter [Handling Sortieren in Ihren Anwendungen](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="4564e-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4564e-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4564e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4564e-113">Informationen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="4564e-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4564e-114">Behandeln von Sortierungen in Ihren Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4564e-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="4564e-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="4564e-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="4564e-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="4564e-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
