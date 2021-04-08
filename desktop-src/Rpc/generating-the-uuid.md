---
title: Die UUID wird erzeugt.
description: Der erste Schritt beim Definieren der Schnittstelle ist die Verwendung des Hilfsprogramms "uuidgen, um einen universellen eindeutigen Bezeichner (UUID) zu generieren.
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Remote Prozedur Aufruf RPC, Tasks, erzeugen der UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856067"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="95915-104">Die UUID wird erzeugt.</span><span class="sxs-lookup"><span data-stu-id="95915-104">Generating the UUID</span></span>

<span data-ttu-id="95915-105">Der erste Schritt beim Definieren der Schnittstelle ist die Verwendung des Hilfsprogramms **"uuidgen** , um einen universellen eindeutigen Bezeichner (UUID) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="95915-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="95915-106">Eine UUID ermöglicht es Client-und Server Anwendungen, sich gegenseitig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="95915-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="95915-107">Das Hilfsprogramm **"uuidgen** (Uuidgen.exe) wird automatisch installiert, wenn Sie das Platform Software Development Kit (SDK) installieren.</span><span class="sxs-lookup"><span data-stu-id="95915-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="95915-108">Mit dem folgenden Befehl wird eine UUID generiert und eine Vorlagen Datei mit dem Namen "Hello. idl" erstellt.</span><span class="sxs-lookup"><span data-stu-id="95915-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="95915-109">**"uuidgen/i/ohello.idl**</span><span class="sxs-lookup"><span data-stu-id="95915-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="95915-110">Die Vorlage "Hello. idl" sieht wie folgt aus (mit einer anderen UUID).</span><span class="sxs-lookup"><span data-stu-id="95915-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




