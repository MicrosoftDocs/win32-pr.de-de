---
title: Die UUID-Schnittstellen Datei
description: Die UUID-Schnittstellen Datei sammelt die Definitionen der Schnittstellen Bezeichner von allen Schnittstellen in der verarbeiteten IDL-Datei.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- Mittel l und com-Mittell, Schnittstellen, Proxy-UUID-Dateien
- Schnittstellen-UUID-Datei (Mitte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713457"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="7a383-105">Die UUID-Schnittstellen Datei</span><span class="sxs-lookup"><span data-stu-id="7a383-105">The Interface UUID File</span></span>

<span data-ttu-id="7a383-106">Die UUID-Schnittstellen Datei sammelt die Definitionen der Schnittstellen Bezeichner von allen Schnittstellen in der verarbeiteten IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="7a383-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="7a383-107">Ähnlich wie bei der Stubdatei und der Header Datei wird die Eingabedaten Stromsperre durch die aktuelle IDL-Datei und die enthaltenen Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="7a383-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="7a383-108">Beispielsweise generiert der Compiler für Interface iface eine Konstante IID \_ iface und initialisiert sie mit der in der IDL-Datei angegebenen UUID der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7a383-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="7a383-109">Client Anwendungen und die Proxy-dll verwenden diese Konstante, um die Schnittstelle zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7a383-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="7a383-110">Der Standardname für eine Schnittstellen-IID-Datei, die aus einer Datei erstellt wird. idl ist File \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="7a383-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="7a383-111">Der [**/IID**](-iid.md) -Compilerschalter überschreibt den Standardnamen der Schnittstellen-UUID-Datei.</span><span class="sxs-lookup"><span data-stu-id="7a383-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




