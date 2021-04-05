---
title: Hasotherclients (Eigenschaft)
description: Hasotherclients (Eigenschaft)
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036992"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="b7b7c-103">Hasotherclients (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7b7c-103">HasOtherClients Property</span></span>

<span data-ttu-id="b7b7c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b7b7c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b7b7c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7b7c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b7b7c-106">Gibt zurück, ob das angegebene Zeichen von anderen Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7b7c-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="b7b7c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b7b7c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b7b7c-108">*Agent*. **Zeichen ("***Merkmal-ID***"). Hasotherclients**</span><span class="sxs-lookup"><span data-stu-id="b7b7c-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="b7b7c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b7b7c-109">Value</span></span>     | <span data-ttu-id="b7b7c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7b7c-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="b7b7c-111">**True**</span><span class="sxs-lookup"><span data-stu-id="b7b7c-111">**True**</span></span>  | <span data-ttu-id="b7b7c-112">Das Zeichen hat andere Clients.</span><span class="sxs-lookup"><span data-stu-id="b7b7c-112">The character has other clients.</span></span>           |
| <span data-ttu-id="b7b7c-113">**False**</span><span class="sxs-lookup"><span data-stu-id="b7b7c-113">**False**</span></span> | <span data-ttu-id="b7b7c-114">Das Zeichen weist keine anderen Clients auf.</span><span class="sxs-lookup"><span data-stu-id="b7b7c-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7b7c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7b7c-115">Remarks</span></span>

<span data-ttu-id="b7b7c-116">Sie können diese Eigenschaft verwenden, um zu bestimmen, ob Ihre Anwendung der einzige oder letzte Client des Zeichens ist, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen).</span><span class="sxs-lookup"><span data-stu-id="b7b7c-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




