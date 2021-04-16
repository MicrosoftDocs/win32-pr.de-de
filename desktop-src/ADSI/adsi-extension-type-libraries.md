---
title: ADSI-Erweiterungstyp Bibliotheken
description: Die Typbibliotheken für Erweiterungen werden nicht zusammengeführt.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI-Erweiterungstyp Bibliotheken ADSI
- Erweiterungen ADSI, erweiterungstypbibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515477"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="b59cc-105">ADSI-Erweiterungstyp Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="b59cc-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="b59cc-106">Die Typbibliotheken für Erweiterungen werden nicht zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="b59cc-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="b59cc-107">ADSI-Clients müssen speziell die Typbibliothek für jede Erweiterung einschließen.</span><span class="sxs-lookup"><span data-stu-id="b59cc-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="b59cc-108">Die Typbibliothek ist für Visual Basic erforderlich, um frühe Bindungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b59cc-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="b59cc-109">Client Anwendungen, die in C/C++ geschrieben wurden, können die **QueryInterface** -Methode für die Erweiterungs Schnittstellen, die in den Erweiterungs Header Dateien definiert sind, abrufen.</span><span class="sxs-lookup"><span data-stu-id="b59cc-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




