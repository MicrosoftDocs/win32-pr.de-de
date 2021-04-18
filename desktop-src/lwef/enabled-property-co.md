---
title: Aktivierte Eigenschaft (Befehls Objekt)
description: Enabled-Eigenschaft
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341345"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="bc670-103">Aktivierte Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="bc670-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="bc670-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bc670-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bc670-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc670-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bc670-106">Gibt zurück oder legt fest, ob der **Befehl** im Popup Menü des angegebenen Zeichens aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bc670-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="bc670-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bc670-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bc670-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_\*_"). Aktivierter_ \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="bc670-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="bc670-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bc670-109">Part</span></span>      | <span data-ttu-id="bc670-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc670-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc670-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="bc670-111">*boolean*</span></span> | <span data-ttu-id="bc670-112">Ein boolescher Ausdruck, der angibt, ob der **Befehl** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bc670-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="bc670-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="bc670-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="bc670-114">Der **Befehl** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc670-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="bc670-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="bc670-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="bc670-116">Der **Befehl** ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc670-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc670-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc670-117">Remarks</span></span>

<span data-ttu-id="bc670-118">Wenn die [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt ist, wird die Beschriftung der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte im Popupmenü des Zeichens als normaler Text angezeigt, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="bc670-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="bc670-119">Wenn die **aktivierte** Eigenschaft **false** ist, wird die Beschriftung als nicht verfügbarer (deaktivierter) Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc670-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="bc670-120">Ein deaktivierter **Befehl** ist auch für die Spracheingabe nicht zugänglich.</span><span class="sxs-lookup"><span data-stu-id="bc670-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

