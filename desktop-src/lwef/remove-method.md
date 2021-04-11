---
title: Remove-Methode
description: Remove-Methode
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315135"
---
# <a name="remove-method"></a><span data-ttu-id="0ca97-103">Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="0ca97-103">Remove Method</span></span>

<span data-ttu-id="0ca97-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0ca97-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0ca97-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ca97-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0ca97-106">Entfernt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0ca97-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="0ca97-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0ca97-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0ca97-108">*Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle. Remove*** Name*</span><span class="sxs-lookup"><span data-stu-id="0ca97-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="0ca97-109">Teil</span><span class="sxs-lookup"><span data-stu-id="0ca97-109">Part</span></span>   | <span data-ttu-id="0ca97-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ca97-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="0ca97-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="0ca97-111">*Name*</span></span> | <span data-ttu-id="0ca97-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0ca97-112">Required.</span></span> <span data-ttu-id="0ca97-113">Ein Zeichen folgen Wert, der der ID für den Befehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="0ca97-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ca97-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ca97-114">Remarks</span></span>

<span data-ttu-id="0ca97-115">Wenn ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der Auflistung entfernt wird, wird es nicht mehr angezeigt, wenn das Popupmenü des Zeichens angezeigt wird, oder im Befehlsfenster, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0ca97-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ca97-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ca97-116">See Also</span></span>

[<span data-ttu-id="0ca97-117">**RemoveAll-Methode**</span><span class="sxs-lookup"><span data-stu-id="0ca97-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 