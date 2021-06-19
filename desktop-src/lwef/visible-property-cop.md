---
title: Visible-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Command-Objekts, das zurückgibt oder festlegt, ob der Befehl im Popupmenü des Zeichens sichtbar ist.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396245"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="28817-103">Visible-Eigenschaft (Befehlsobjekt)</span><span class="sxs-lookup"><span data-stu-id="28817-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="28817-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="28817-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28817-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28817-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28817-106">Gibt zurück oder legt fest, ob der [**Befehl**](/windows/desktop/lwef/the-command-object) im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="28817-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="28817-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="28817-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="28817-108">*agent\***. Characters(**"* CharacterID *"**). Commands(**"* name *"\*\*). Sichtbarer* \*  \[  =  *boolescher Wert*\]</span><span class="sxs-lookup"><span data-stu-id="28817-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="28817-109">Teil</span><span class="sxs-lookup"><span data-stu-id="28817-109">Part</span></span>      | <span data-ttu-id="28817-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28817-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28817-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="28817-111">*boolean*</span></span> | <span data-ttu-id="28817-112">Ein boolescher Ausdruck, der angibt, ob die Beschriftung des [**Befehls**](/windows/desktop/lwef/the-command-object)im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="28817-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="28817-113">**True** (Standard) Die Beschriftung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28817-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="28817-114">**False** Die Beschriftung wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28817-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28817-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28817-115">Remarks</span></span>

<span data-ttu-id="28817-116">Legen Sie diese Eigenschaft auf **False** fest, wenn Sie Spracheingaben für Ihre eigenen Schnittstellen einschließen möchten, ohne dass sie im Popupmenü für das Zeichen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28817-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="28817-117">Wenn Sie die [**Caption-Eigenschaft**](caption-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) auf die leere Zeichenfolge ("") festlegen, wird der Beschriftungstext unabhängig von der [](visible-property.md) Visible-Eigenschaftseinstellung nicht im Popupmenü angezeigt (z. B. als leere Zeile).</span><span class="sxs-lookup"><span data-stu-id="28817-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="28817-118">Die [](visible-property.md) Visible-Eigenschafteneinstellung der [**übergeordneten Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) wirkt sich nicht auf die **Visible-Eigenschafteneinstellung** des **Befehls** aus.</span><span class="sxs-lookup"><span data-stu-id="28817-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

