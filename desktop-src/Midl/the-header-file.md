---
title: Die Header Datei
description: Die Header Datei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den in der \ include-Direktive enthaltenen Dateien deklariert werden.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- Mittel l-und RPC-Mittell, Schnittstellen, Header Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037297"
---
# <a name="the-header-file"></a><span data-ttu-id="b8040-104">Die Header Datei</span><span class="sxs-lookup"><span data-stu-id="b8040-104">The Header File</span></span>

<span data-ttu-id="b8040-105">Die Header Datei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den in der include-Direktive enthaltenen Dateien deklariert werden \# .</span><span class="sxs-lookup"><span data-stu-id="b8040-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="b8040-106">Datentypen aus den Dateien, die mit der Import-Anweisung importiert werden, werden nicht in die Header Datei repliziert. Stattdessen enthält die generierte Header Datei eine include-Zeile zur H-Datei, die aus der importierten Datei generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b8040-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="b8040-107">Die Header Datei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufzurufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b8040-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="b8040-108">Die Mittel-Compilerschalter [**/Header**](-header.md) und [**/out**](-out.md) wirken sich auf die Header Datei aus.</span><span class="sxs-lookup"><span data-stu-id="b8040-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




