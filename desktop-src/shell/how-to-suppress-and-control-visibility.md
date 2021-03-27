---
description: In diesem Thema erfahren Sie, wie Sie die Sichtbarkeit des Verbs steuern.
title: Unterdrücken der Sichtbarkeit des Verbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215938"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="3080d-103">Unterdrücken der Sichtbarkeit des Verbs</span><span class="sxs-lookup"><span data-stu-id="3080d-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="3080d-104">In diesem Thema erfahren Sie, wie Sie die Sichtbarkeit des Verbs steuern.</span><span class="sxs-lookup"><span data-stu-id="3080d-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="3080d-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="3080d-105">Instructions</span></span>


<span data-ttu-id="3080d-106">Sie können Windows-Richtlinien Einstellungen verwenden, um die Sichtbarkeit zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3080d-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="3080d-107">Verben können durch Richtlinien Einstellungen unterdrückt werden, indem Sie dem Registrierungs Unterschlüssel des Verbs einen **SuppressionPolicy** -Unterschlüssel oder einen **suppressionpolicyex** -GUID-Wert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3080d-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="3080d-108">Legen Sie den Wert des unter Schlüssels **SuppressionPolicy** auf die Richtlinien-ID fest.</span><span class="sxs-lookup"><span data-stu-id="3080d-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="3080d-109">Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenü Eintrag unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="3080d-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="3080d-110">Mögliche Richtlinien-ID-Werte finden Sie unter der [**Einschränkungs**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="3080d-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 



