---
title: Count-Eigenschaft
description: Count-Eigenschaft
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858191"
---
# <a name="count-property"></a><span data-ttu-id="73107-103">Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73107-103">Count Property</span></span>

<span data-ttu-id="73107-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="73107-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="73107-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73107-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="73107-106">Gibt eine lange Ganzzahl (schreibgeschützte Eigenschaft) zurück, die die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="73107-106">Returns a Long integer (read-only property) that specifies the count of [**Command**](/windows/desktop/lwef/the-command-object) objects in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="73107-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="73107-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="73107-108">*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Befehle. Count**</span><span class="sxs-lookup"><span data-stu-id="73107-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Count*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73107-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73107-109">Remarks</span></span>

<span data-ttu-id="73107-110">**Count** schließt nur die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte ein, die Sie in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren.</span><span class="sxs-lookup"><span data-stu-id="73107-110">**Count** includes only the number of [**Command**](/windows/desktop/lwef/the-command-object) objects you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="73107-111">Server-oder andere Client Einträge sind nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="73107-111">Server or other client entries are not included.</span></span>

 

 