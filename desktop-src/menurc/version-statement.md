---
title: Versions Anweisung
description: Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menüs der Versions Anweisung und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718510"
---
# <a name="version-statement"></a><span data-ttu-id="df9c6-104">Versions Anweisung</span><span class="sxs-lookup"><span data-stu-id="df9c6-104">VERSION statement</span></span>

<span data-ttu-id="df9c6-105">Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="df9c6-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="df9c6-106">Der angegebene *DWORD* -Wert wird mit der Ressource in der kompilierten angezeigt. RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="df9c6-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="df9c6-107">Der Wert wird jedoch nicht in der ausführbaren Datei gespeichert und hat keine Bedeutung für das System.</span><span class="sxs-lookup"><span data-stu-id="df9c6-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="df9c6-108">Die **Version** -Anweisung wird vor dem Anfang des Texts der Ressourcendefinition " [**Accelerators**](accelerators-resource.md)", " [**DIALOGEX**](dialogex-resource.md)", " [**Menu**](menu-resource.md)", " [**RCDATA**](rcdata-resource.md)" oder " [**STRINGTABLE**](stringtable-resource.md) " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df9c6-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="df9c6-109">Der angegebene Wert gilt nur für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="df9c6-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="df9c6-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="df9c6-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="df9c6-111">Ein benutzerdefinierter **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="df9c6-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="df9c6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df9c6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9c6-113">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="df9c6-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="df9c6-114">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="df9c6-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="df9c6-115">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="df9c6-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="df9c6-116">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="df9c6-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="df9c6-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="df9c6-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="df9c6-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="df9c6-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




