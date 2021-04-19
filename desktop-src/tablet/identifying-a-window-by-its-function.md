---
description: Beschreibung, wie ein Fenster durch seine Funktion für den Tablet PC identifiziert wird.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identifizieren eines Fensters anhand seiner Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353098"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="026cd-103">Identifizieren eines Fensters anhand seiner Funktion</span><span class="sxs-lookup"><span data-stu-id="026cd-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="026cd-104">Identifizieren Sie jede Art von Fenster, indem Sie Ihr eine eindeutige Fenster Klasse zuweisen.</span><span class="sxs-lookup"><span data-stu-id="026cd-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="026cd-105">Vermeiden Sie eine einzelne Fenster Klasse, die für eine Vielzahl von Funktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="026cd-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="026cd-106">Barrierefreiheits Hilfen müssen über diese Identifikation verfügen, damit unterschiedliche Fenster in derselben Anwendung behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="026cd-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="026cd-107">Möglicherweise gibt es separate Anweisungen für die Handhabung dieser Fenster, z. b. das ankündigen bestimmter Bereiche, wenn sich der Inhalt ändert.</span><span class="sxs-lookup"><span data-stu-id="026cd-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="026cd-108">Wenn Sie keine separaten Fenster Klassen verwenden können, können Sie die Unterschiede über Microsoft <entity type="reg"/> Active Accessibility <entity type="reg"/> oder ggf. durch eine private Fenster Meldung, die Sie auf Ihrer Website dokumentieren, verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="026cd-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="026cd-109">Weitere Informationen zum verfügbar machen von Fenster Klassen mithilfe Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="026cd-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
