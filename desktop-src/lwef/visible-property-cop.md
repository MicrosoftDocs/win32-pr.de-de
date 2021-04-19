---
title: Visible-Eigenschaft (Befehls Objekt)
description: Visible-Eigenschaft
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106342391"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="eaf98-103">Visible-Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="eaf98-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="eaf98-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="eaf98-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eaf98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eaf98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eaf98-106">Gibt zurück oder legt fest, ob der [**Befehl**](/windows/desktop/lwef/the-command-object) im Popupmenü des Zeichens sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="eaf98-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="eaf98-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="eaf98-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="eaf98-108">\*Agent \***. Zeichen (**"\* Merkmal-ID *"**). Befehle (**"* Name \*" \* *). Sichtbarer* \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="eaf98-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="eaf98-109">Teil</span><span class="sxs-lookup"><span data-stu-id="eaf98-109">Part</span></span>      | <span data-ttu-id="eaf98-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaf98-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf98-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="eaf98-111">*boolean*</span></span> | <span data-ttu-id="eaf98-112">Ein boolescher Ausdruck, der angibt, ob die Beschriftung des [**Befehls**](/windows/desktop/lwef/the-command-object)im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eaf98-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="eaf98-113">**True** (Standard) die Beschriftung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eaf98-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="eaf98-114">**False** Die Beschriftung wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eaf98-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaf98-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaf98-115">Remarks</span></span>

<span data-ttu-id="eaf98-116">Legen Sie diese Eigenschaft auf " **false** " fest, wenn Sie Spracheingaben für Ihre eigenen Schnittstellen einschließen möchten, ohne dass Sie im Popup Menü für das Zeichen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eaf98-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="eaf98-117">Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts auf die leere Zeichenfolge ("") festlegen, wird der Beschriftungs Text nicht im Popup Menü (z. b. als Leerzeile) angezeigt, unabhängig von dessen [**sichtbarer**](visible-property.md) Eigenschaften Einstellung.</span><span class="sxs-lookup"><span data-stu-id="eaf98-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="eaf98-118">Die [**Visible**](visible-property.md) -Eigenschaften Einstellung der Auflistung der übergeordneten [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts wirkt sich nicht auf die **sichtbare** Eigenschafts Einstellung des **Befehls** aus.</span><span class="sxs-lookup"><span data-stu-id="eaf98-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

