---
title: UI-Richtlinien für NDF-Hilfsklassen Erweiterungen
description: Beim Erstellen einer Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparatur Schritte besser verstehen kann.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313584"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="d85c5-103">UI-Richtlinien für NDF-Hilfsklassen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="d85c5-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="d85c5-104">Beim Erstellen einer Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparatur Schritte besser verstehen kann.</span><span class="sxs-lookup"><span data-stu-id="d85c5-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="d85c5-105">Grundursache und Reparatur</span><span class="sxs-lookup"><span data-stu-id="d85c5-105">Root Cause and Repair</span></span>

<span data-ttu-id="d85c5-106">Wenn ein Incident auftritt, wird ein Dialogfeld angezeigt, um den Benutzer darüber zu informieren, was passiert ist.</span><span class="sxs-lookup"><span data-stu-id="d85c5-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="d85c5-107">Der von Ihnen erstellte Text wird in zwei separaten Bereichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d85c5-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="d85c5-108">**Grundursache**: eine kurze Beschreibung der Ursache des Problems.</span><span class="sxs-lookup"><span data-stu-id="d85c5-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="d85c5-109">Enthält Informationen, die einem Administrator oder einem erweiterten Benutzer helfen, das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d85c5-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="d85c5-110">**Reparatur** Vorgang: erweitert die Grundursache, um weitere Details zu den Schritten zu erhalten, die ein Benutzer ausführen kann, ohne zu lange zu lange.</span><span class="sxs-lookup"><span data-stu-id="d85c5-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="d85c5-111">Jede Grundursache oder Reparatur sollte über einen Titel und eine Beschreibung verfügen.</span><span class="sxs-lookup"><span data-stu-id="d85c5-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="d85c5-112">Der gesamte Text vor dem ersten " \\ n"-Zeichen wird für den Titel verwendet.</span><span class="sxs-lookup"><span data-stu-id="d85c5-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="d85c5-113">Der gesamte Text, der auf das erste \\ Zeichen "n" folgt (einschließlich aller nachfolgenden Zeilenumbrüche), wird für die Beschreibung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d85c5-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="d85c5-114">Titel Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d85c5-114">Title Guidelines</span></span>

<span data-ttu-id="d85c5-115">Der Titel einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:</span><span class="sxs-lookup"><span data-stu-id="d85c5-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="d85c5-116">Darf höchstens 128 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="d85c5-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="d85c5-117">(es werden 40 Zeichen oder weniger Zeichen empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="d85c5-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="d85c5-118">Darf nicht mit einem-Zeitraum enden.</span><span class="sxs-lookup"><span data-stu-id="d85c5-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="d85c5-119">Beschreibungen von Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d85c5-119">Description Guidelines</span></span>

<span data-ttu-id="d85c5-120">Die Beschreibung einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:</span><span class="sxs-lookup"><span data-stu-id="d85c5-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="d85c5-121">Darf höchstens 512 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="d85c5-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="d85c5-122">Jeder Satz sollte mit einem bestimmten Zeitraum enden.</span><span class="sxs-lookup"><span data-stu-id="d85c5-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="d85c5-123">Das \\ Zeichen "n" kann verwendet werden, um einen Zeilenumbruch in der Beschreibung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d85c5-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




