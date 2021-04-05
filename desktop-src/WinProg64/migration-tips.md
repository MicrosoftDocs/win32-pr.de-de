---
title: Tipps zur Migration
description: Es ist wichtig, Adress Berechnungen und Zeigerarithmetik zu berücksichtigen, wenn Sie Ihren Code auf 64-Bit-Fenster portieren.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Tipps zur Migration
- Migrations Tipps 64-Bit-Windows-Programmierung
- Kompatibilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711711"
---
# <a name="migration-tips"></a><span data-ttu-id="7c252-106">Tipps zur Migration</span><span class="sxs-lookup"><span data-stu-id="7c252-106">Migration Tips</span></span>

<span data-ttu-id="7c252-107">Bei der Untersuchung des Codes für die 64-Bit-Kompatibilität sind die folgenden beiden Hauptbereiche von Bedeutung:</span><span class="sxs-lookup"><span data-stu-id="7c252-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="7c252-108">Adress Berechnungen</span><span class="sxs-lookup"><span data-stu-id="7c252-108">Address calculations</span></span>
-   <span data-ttu-id="7c252-109">Zeigerarithmetik</span><span class="sxs-lookup"><span data-stu-id="7c252-109">Pointer arithmetic</span></span>

<span data-ttu-id="7c252-110">Aus vielen Gründen haben Entwickler Adressen als **ulong** -Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7c252-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="7c252-111">Schließlich sind auf 32-Bit-Fenstern eine Adresse, ein Zeiger und ein **ulong** -Wert alle 32 Bits lang.</span><span class="sxs-lookup"><span data-stu-id="7c252-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="7c252-112">Bei 64-Bit-Fenstern weisen jedoch eine Adresse und ein **ulong** nicht die gleiche Länge auf.</span><span class="sxs-lookup"><span data-stu-id="7c252-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="7c252-113">Während ein **ulong** -Wert ein 32-Bit-Wert ist, sind alle Zeiger jetzt 64-Bit-Werte.</span><span class="sxs-lookup"><span data-stu-id="7c252-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c252-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7c252-114">In this Section</span></span>

-   [<span data-ttu-id="7c252-115">Allgemeine Richtlinien für die Portierung</span><span class="sxs-lookup"><span data-stu-id="7c252-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="7c252-116">Speichern eines 64-Bit-Werts</span><span class="sxs-lookup"><span data-stu-id="7c252-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="7c252-117">Häufige Compilerfehler</span><span class="sxs-lookup"><span data-stu-id="7c252-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="7c252-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="7c252-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




