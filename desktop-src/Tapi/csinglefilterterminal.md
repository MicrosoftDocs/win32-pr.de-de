---
description: Csinglefilterterminal ist eine zusätzliche Terminal-Basisklasse, die sowohl auf statische als auch dynamische Terminals anwendbar ist.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: Csinglefilterterminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357886"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="6e6a2-103">Csinglefilterterminal</span><span class="sxs-lookup"><span data-stu-id="6e6a2-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="6e6a2-104">**Csinglefilterterminal** ist eine zusätzliche Terminal-Basisklasse, die sowohl auf statische als auch dynamische Terminals anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="6e6a2-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="6e6a2-105">Sie wird von [**cbaseterminal**](cbaseterminal.md) abgeleitet und vereinfacht die Implementierung, indem angenommen wird, dass das Terminal über einen einzelnen DirectShow-Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="6e6a2-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="6e6a2-106">Wenn diese Bedingung erfüllt ist, ist das Ableiten einer Terminal Implementierung von **csinglefilterterminal** wesentlich einfacher als die Ableitung von **cbaseterminal**.</span><span class="sxs-lookup"><span data-stu-id="6e6a2-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="6e6a2-107">Definiert in "mspterm. h".</span><span class="sxs-lookup"><span data-stu-id="6e6a2-107">Defined in MSPterm.h.</span></span>

 

 



