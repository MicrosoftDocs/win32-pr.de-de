---
title: Funktions Datentypen und Rückgabewerte
description: Funktions Datentypen und Rückgabewerte
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947636"
---
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="76f2f-103">Funktions Datentypen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="76f2f-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="76f2f-104">Die avifile-Funktionen und-Makros verwenden Datei-und Datenstrom Handler, die mit OLE-Technologie implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="76f2f-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="76f2f-105">Der Standard Datentyp einer OLE-Funktion ist **STDAPI**, und die Funktion gibt einen **HRESULT** -Wert (0 für Erfolg oder andernfalls einen Fehler) zurück.</span><span class="sxs-lookup"><span data-stu-id="76f2f-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="76f2f-106">Wenn eine Funktion einen anderen Wert als ein **HRESULT** zurückgibt, hat der Typ des Prototyps der Funktion eine etwas andere Syntax, die den Rückgabe Werttyp in Klammern nach "STDAPI" einbettet \_ .</span><span class="sxs-lookup"><span data-stu-id="76f2f-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="76f2f-107">Beispielsweise wird von einer Funktion, die einen **Long** -Datenwert zurückgibt, **STDAPI \_ (Long)** in der Prototype-Anweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="76f2f-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




