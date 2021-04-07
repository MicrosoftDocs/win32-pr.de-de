---
title: DefaultCommand (Eigenschaft)
description: DefaultCommand (Eigenschaft)
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038915"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="f14a8-103">DefaultCommand (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f14a8-103">DefaultCommand Property</span></span>

<span data-ttu-id="f14a8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f14a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f14a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f14a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f14a8-106">Gibt den Standardbefehl für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f14a8-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="f14a8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f14a8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f14a8-108">*Agent. \* \* \* Zeichen* \*  **("***Merkmal-ID***"). Commands. DefaultCommand** - \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="f14a8-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="f14a8-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f14a8-109">Part</span></span>     | <span data-ttu-id="f14a8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f14a8-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f14a8-111">*string*</span><span class="sxs-lookup"><span data-stu-id="f14a8-111">*string*</span></span> | <span data-ttu-id="f14a8-112">Ein Zeichen folgen Wert, der den Namen (ID) des [**Befehls**](/windows/desktop/lwef/the-command-object)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f14a8-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f14a8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f14a8-113">Remarks</span></span>

<span data-ttu-id="f14a8-114">Diese Eigenschaft ermöglicht es Ihnen, einen [**Befehl**](/windows/desktop/lwef/the-command-object) in der [**Befehls Auflistung**](/windows/desktop/lwef/the-commands-collection-object) als Standardbefehl festzulegen, wodurch er fett formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="f14a8-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="f14a8-115">Dies ändert nicht die Befehls Behandlung oder Doppelklick Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f14a8-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="f14a8-116">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="f14a8-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 