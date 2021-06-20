---
title: Enabled-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die Enabled Command-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407333"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="ba840-104">Enabled-Eigenschaft (Command-Objekt)</span><span class="sxs-lookup"><span data-stu-id="ba840-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="ba840-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ba840-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ba840-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba840-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ba840-107">Gibt zurück oder legt fest, ob der **Befehl** im Popupmenü des angegebenen Zeichens aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba840-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="ba840-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ba840-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ba840-109">*agent\***. Zeichen ("**_CharacterID_*_"). Commands("_*_name_*_")._ \*  \[  =  *Boolescher Wert* aktiviert\]</span><span class="sxs-lookup"><span data-stu-id="ba840-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="ba840-110">Teil</span><span class="sxs-lookup"><span data-stu-id="ba840-110">Part</span></span>      | <span data-ttu-id="ba840-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba840-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba840-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="ba840-112">*boolean*</span></span> | <span data-ttu-id="ba840-113">Ein boolescher Ausdruck, der angibt, ob der **Befehl** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba840-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="ba840-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="ba840-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="ba840-115">Der **Befehl** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba840-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="ba840-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ba840-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="ba840-117">Der **Befehl** ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba840-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba840-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba840-118">Remarks</span></span>

<span data-ttu-id="ba840-119">Wenn die [**Enabled-Eigenschaft**](enabled-property.md) auf **True** festgelegt ist, wird die Beschriftung der [**Command-Objekte**](/windows/desktop/lwef/the-command-object) als normaler Text im Popupmenü des Zeichens angezeigt, wenn die Clientanwendung eingabeaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ba840-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="ba840-120">Wenn die **Enabled-Eigenschaft** **False** lautet, wird die Beschriftung als nicht verfügbarer (deaktivierter) Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba840-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="ba840-121">Auf einen deaktivierten **Befehl** kann auch für die Spracheingabe nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="ba840-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

