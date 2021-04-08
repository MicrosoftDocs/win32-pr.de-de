---
description: ICE89 überprüft, ob der Wert in der übergeordneten ProgID-Spalte in der ProgID- \_ Tabelle ein gültiger Fremdschlüssel in der ProgID-Spalte in der ProgID-Tabelle ist. Jedes übergeordnete ProgID-Element muss einen Datensatz in der ProgID-Tabelle aufweisen.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960481"
---
# <a name="ice89"></a><span data-ttu-id="48071-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="48071-104">ICE89</span></span>

<span data-ttu-id="48071-105">ICE89 überprüft, ob der Wert in der übergeordneten ProgID-Spalte in der ProgID- \_ [Tabelle](progid-table.md) ein gültiger Fremdschlüssel in der ProgID-Spalte in der ProgID-Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="48071-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="48071-106">Jedes übergeordnete ProgID-Element muss einen Datensatz in der ProgID-Tabelle aufweisen.</span><span class="sxs-lookup"><span data-stu-id="48071-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="48071-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="48071-107">Result</span></span>

<span data-ttu-id="48071-108">ICE89 gibt die folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="48071-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="48071-109">ICE89-Fehler</span><span class="sxs-lookup"><span data-stu-id="48071-109">ICE89 error</span></span>                                                           | <span data-ttu-id="48071-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48071-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="48071-111">Das übergeordnete ProgID-Element \_ ' \[ 1 \] ' in der ProgID-Tabelle ist keine gültige ProgID.</span><span class="sxs-lookup"><span data-stu-id="48071-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="48071-112">Es wurde eine übergeordnete ProgID angegeben, die nicht in der ProgID-Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="48071-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="48071-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48071-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48071-114">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="48071-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



