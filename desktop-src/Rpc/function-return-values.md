---
title: Funktions Rückgabewerte
description: Funktions Rückgabewerte ähneln "\ out \"-Parametern, da Ihre Daten nicht durch die Client Anwendung bereitgestellt werden.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342372"
---
# <a name="function-return-values"></a><span data-ttu-id="21a32-103">Funktions Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="21a32-103">Function Return Values</span></span>

<span data-ttu-id="21a32-104">Funktions Rückgabewerte ähneln reinen **\[ out \]**-Parametern, da Ihre Daten nicht durch die Client Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="21a32-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="21a32-105">Sie werden jedoch anders verwaltet.</span><span class="sxs-lookup"><span data-stu-id="21a32-105">However they are managed differently.</span></span> <span data-ttu-id="21a32-106">Im Gegensatz zu reinen **\[ out \]**-Parametern müssen Sie keine Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="21a32-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="21a32-107">Die Remote Prozedur kann jeden gültigen Datentyp außer Verweis Zeigern und nicht gekapselten Unions zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="21a32-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="21a32-108">Es wird jedoch empfohlen, einen **\[ out \]** -Parameter anstelle eines Rückgabewerts für komplexe Datentypen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="21a32-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="21a32-109">Beim zurückgeben komplexer Datentypen generiert der Mittelwert Compiler einen/OS-modusstub.</span><span class="sxs-lookup"><span data-stu-id="21a32-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="21a32-110">Folglich gehen alle kürzlich von/robust bereitgestellten Fehler Überprüfungs Informationen verloren.</span><span class="sxs-lookup"><span data-stu-id="21a32-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="21a32-111">Funktions Rückgabewerte, bei denen es sich um Zeiger Typen handelt, werden vom Clientstub mit einem aufzurufenden [ \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1)Zuordnungs Befehl zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="21a32-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="21a32-112">Dementsprechend kann nur das Unique-Attribut oder das Full-Zeiger Attribut auf einen Zeiger Funktions Rückgabetyp angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="21a32-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 