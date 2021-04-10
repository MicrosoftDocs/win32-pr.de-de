---
description: ICE49 prüft standardmäßige Registrierungseinträge, bei denen es sich nicht um einen reg \_ SZ-Typ handelt.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867295"
---
# <a name="ice49"></a><span data-ttu-id="9b727-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="9b727-103">ICE49</span></span>

<span data-ttu-id="9b727-104">ICE49 prüft standardmäßige Registrierungseinträge, bei denen es sich nicht um einen **reg \_ SZ** -Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="9b727-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="9b727-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="9b727-105">Result</span></span>

<span data-ttu-id="9b727-106">ICE49 gibt eine Warnung aus, wenn ein Standard Registrierungs Eintrag vorhanden ist, bei dem es sich nicht um einen **reg \_ SZ** -Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="9b727-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="9b727-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b727-107">Example</span></span>

<span data-ttu-id="9b727-108">ICE49 meldet die folgende Warnung für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="9b727-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="9b727-109">Der Wert " \# 123" ist ein **DWORD** -Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="9b727-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="9b727-110">[Registrierungs Tabelle](registry-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="9b727-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="9b727-111">Registrierung</span><span class="sxs-lookup"><span data-stu-id="9b727-111">Registry</span></span> | <span data-ttu-id="9b727-112">Name</span><span class="sxs-lookup"><span data-stu-id="9b727-112">Name</span></span> | <span data-ttu-id="9b727-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9b727-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="9b727-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="9b727-114">Reg1</span></span>     |      | <span data-ttu-id="9b727-115">\#123</span><span class="sxs-lookup"><span data-stu-id="9b727-115">\#123</span></span> |



 

<span data-ttu-id="9b727-116">Um diese Warnung zu beheben, ändern Sie den Wert in Typ **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="9b727-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="9b727-117">Komponenten mit nicht-**reg- \_ SZ** sind gültig.</span><span class="sxs-lookup"><span data-stu-id="9b727-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b727-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b727-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b727-119">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="9b727-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="9b727-120">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="9b727-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



