---
description: Im folgenden finden Sie einige allgemeine Instanzen von Bedingungs Anweisungen. Weitere Informationen finden Sie unter bedingte Anweisungs Syntax.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Beispiele für bedingte Anweisungs Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959438"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="8f7c4-104">Beispiele für bedingte Anweisungs Syntax</span><span class="sxs-lookup"><span data-stu-id="8f7c4-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="8f7c4-105">Im folgenden finden Sie einige allgemeine Instanzen von Bedingungs Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="8f7c4-106">Weitere Informationen finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8f7c4-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="8f7c4-107">Aktion beim Entfernen ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-107">Run action on removal.</span></span>

<span data-ttu-id="8f7c4-108">Weitere Informationen finden Sie unter durch [führen von während des Entfernens](conditioning-actions-to-run-during-removal.md)auszuführenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="8f7c4-109">Führen Sie die Aktion nur aus, wenn das Produkt nicht installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="8f7c4-110">Führen Sie die Aktion nur aus, wenn das Produkt lokal installiert wird.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="8f7c4-111">Führen Sie die Aktion bei einer erneuten Installation nicht aus.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="8f7c4-112">Der Begriff "&Featurename = 3" bedeutet, dass die Funktion lokal installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="8f7c4-113">Der Begriff "Not (! Featurename = 3) "bedeutet, dass das Feature nicht lokal installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="8f7c4-114">Aktion nur ausführen, wenn die Funktion deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="8f7c4-115">Diese Bedingung überprüft nur, ob die Funktion vom installierten Zustand "lokal" in den Zustand "nicht vorhanden" übergeht.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="8f7c4-116">Die Aktion wird nur ausgeführt, wenn die Komponente lokal installiert wurde, sich jedoch außerhalb des Zustands befindet.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="8f7c4-117">Der Begriff "? Componetname = 3 "bedeutet, dass die Komponente lokal installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="8f7c4-118">Der Begriff "$ComponentName = 2" bedeutet, dass der Aktionszustand für die Komponente nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="8f7c4-119">Der Begriff "$ComponentName = 4" bedeutet, dass der Aktionszustand für die Komponente aus der Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="8f7c4-120">Beachten Sie, dass der Aktions Status ankündigen für eine Komponente nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="8f7c4-121">Aktion nur für die Neuinstallation einer Komponente ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="8f7c4-122">Aktion nur ausführen, wenn ein bestimmter Patch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="8f7c4-123">Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Eigenschaften Seite " [**Patch**](patch.md) ".</span><span class="sxs-lookup"><span data-stu-id="8f7c4-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



