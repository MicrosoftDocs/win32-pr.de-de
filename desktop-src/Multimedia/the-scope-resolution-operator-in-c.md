---
title: Der Bereichs Auflösungs Operator in C++
description: Der Bereichs Auflösungs Operator in C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856203"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="7251e-103">Der Bereichs Auflösungs Operator in C++</span><span class="sxs-lookup"><span data-stu-id="7251e-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="7251e-104">Zwei Doppelpunkte (::) werden in C++ als *Bereichs Auflösungs* Operator verwendet.</span><span class="sxs-lookup"><span data-stu-id="7251e-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="7251e-105">Dieser Operator bietet Ihnen mehr Freiheit beim Benennen Ihrer Variablen, indem Sie die Unterscheidung zwischen Variablen mit demselben Namen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7251e-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="7251e-106">*MyFile:: Read* bezieht sich z. b. auf die *Read* -Methode der *MyFile* -Klasse von Objekten, im Gegensatz zu *Yourfile:: Read*, die auf eine *Read* -Methode in der *Yourfile* -Klasse verweist.</span><span class="sxs-lookup"><span data-stu-id="7251e-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




