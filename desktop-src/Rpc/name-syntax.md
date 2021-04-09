---
title: Namens Syntax
description: Remote Prozedur Aufruf (RPC) und namens Syntax.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947899"
---
# <a name="name-syntax"></a><span data-ttu-id="de6b9-103">Namens Syntax</span><span class="sxs-lookup"><span data-stu-id="de6b9-103">Name Syntax</span></span>

<span data-ttu-id="de6b9-104">Microsoft RPC akzeptiert Namen, die der folgenden Syntax entsprechen:</span><span class="sxs-lookup"><span data-stu-id="de6b9-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="de6b9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="de6b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de6b9-106"><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="de6b9-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="de6b9-107">Gibt einen Bezeichner an, der ein beliebiges Zeichen außer dem Trennzeichen-Schrägstrich (/) enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="de6b9-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="de6b9-108"><span id="domainname"></span><span id="DOMAINNAME"></span>Domain Name</span><span class="sxs-lookup"><span data-stu-id="de6b9-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="de6b9-109">Gibt den Namen der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="de6b9-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="de6b9-110">Ein Parameter, mit dem der Name der Syntax ausgewählt wird, und die Zeichenfolge, die den Namen angibt, werden für viele der NSI-RPC-Funktionen (Name Service Interface) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="de6b9-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="de6b9-111">Nur ein Name-Syntax-Typ wird von Microsoft RPC unterstützt, wie in der DCE-Syntax des Konstanten RPC \_ C \_ NS angegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="de6b9-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="de6b9-112">Diese Konstante wird in der Header Datei "rpcnsi. H" definiert.</span><span class="sxs-lookup"><span data-stu-id="de6b9-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="de6b9-113">Die von der RPC- \_ C- \_ NS-Syntax DCE angegebene namens Syntax \_ \_ ist eine Erweiterung der namens Syntax des OSF- \_ DCE-Zell Verzeichnis Dienstanbieter (CDs).</span><span class="sxs-lookup"><span data-stu-id="de6b9-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="de6b9-114">Die Möglichkeit, einen Domänen Namen anzugeben, stellt eine Erweiterung dieser Syntax dar.</span><span class="sxs-lookup"><span data-stu-id="de6b9-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="de6b9-115">Es gibt keine absolute Beschränkung für die Anzahl von Namen, die durch Schrägstriche getrennt werden können, solange die Gesamt Zeichenfolge kleiner als 256 Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="de6b9-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="de6b9-116">Mithilfe der Schrägstriche können Sie eine logische Struktur zum Namen angeben, aber Sie entsprechen nicht einer logischen Struktur in den Objekten selbst.</span><span class="sxs-lookup"><span data-stu-id="de6b9-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




