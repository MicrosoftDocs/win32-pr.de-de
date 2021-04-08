---
description: Mergemodule funktionieren nur mit-Komponenten und nicht mit-Funktionen. Einige Tabellen in Mergemodulen, wie z. b. die PublishComponent-Tabelle, enthalten jedoch Felder, die auf Funktionen verweisen.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Verweisen auf Features in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959658"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="b96f9-104">Verweisen auf Features in Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="b96f9-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="b96f9-105">Mergemodule funktionieren nur mit-Komponenten und nicht mit-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b96f9-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="b96f9-106">Einige Tabellen in Mergemodulen, wie z. b. die [PublishComponent-Tabelle](publishcomponent-table.md), enthalten jedoch Felder, die auf Funktionen verweisen.</span><span class="sxs-lookup"><span data-stu-id="b96f9-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="b96f9-107">Eine NULL-GUID: {00000000-0000-0000-0000-000000000000} muss in einem beliebigen Feld einer mergemoduldatenbank erstellt werden, die auf eine Funktion verweist.</span><span class="sxs-lookup"><span data-stu-id="b96f9-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="b96f9-108">Wenn das Mergemodul in ein Installationspaket zusammengeführt wird, ersetzt das Mergetool die NULL-GUID durch die im Installationspaket angegebene Funktion, mit Ausnahme von Tabellen, die eine besondere Behandlung erfordern, wie z. b. die [ModuleSignature-Tabelle](modulesignature-table.md) und die modulesequence-Tabellen.</span><span class="sxs-lookup"><span data-stu-id="b96f9-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="b96f9-109">Wenn eine NULL-GUID als Primärschlüssel verwendet wird, ist nicht sichergestellt, dass der durch das Mergetool ersetzte Wert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="b96f9-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="b96f9-110">Autoren von Mergemodulen sind dafür verantwortlich, sicherzustellen, dass kein vorhandener Primärschlüssel in der Benutzeroberfläche dupliziert wird, wenn das Mergetool NULL-GUIDs durch Funktionen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b96f9-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



