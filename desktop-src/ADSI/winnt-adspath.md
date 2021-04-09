---
title: WinNT ADsPath
description: Dieses Thema enthält Beispiele für Zeichen folgen, die für den WinNT ADsPath verwendet werden.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947318"
---
# <a name="winnt-adspath"></a><span data-ttu-id="1c0e4-105">WinNT ADsPath</span><span class="sxs-lookup"><span data-stu-id="1c0e4-105">WinNT ADsPath</span></span>

<span data-ttu-id="1c0e4-106">Die ADsPath-Zeichenfolge für den ADSI WinNT-Anbieter kann eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="1c0e4-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="1c0e4-107">Der Domänen Name kann entweder ein NetBIOS-Name oder ein DNS-Name sein.</span><span class="sxs-lookup"><span data-stu-id="1c0e4-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="1c0e4-108">Der Server ist der Name eines bestimmten Servers innerhalb der Domäne.</span><span class="sxs-lookup"><span data-stu-id="1c0e4-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="1c0e4-109">Der Pfad ist der Pfad für ein Objekt, z. b. "printserver1/printer2".</span><span class="sxs-lookup"><span data-stu-id="1c0e4-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="1c0e4-110">Der Objektname ist der Name eines bestimmten Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c0e4-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="1c0e4-111">Die Objektklasse ist der Klassenname des benannten Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c0e4-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="1c0e4-112">Ein Beispiel für diese Verwendung wäre "Winnt://MyServer/JeffSmith,User".</span><span class="sxs-lookup"><span data-stu-id="1c0e4-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="1c0e4-113">Die Angabe eines Klassen namens kann die Leistung des Bindungs Vorgangs verbessern.</span><span class="sxs-lookup"><span data-stu-id="1c0e4-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




