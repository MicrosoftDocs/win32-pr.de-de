---
description: Einführung in die Verwendung von Steuerelementen ohne Beschriftung-Eigenschaften für den Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Steuerelemente ohne Beschriftung-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524379"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="19dd5-103">Steuerelemente ohne Beschriftung-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19dd5-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="19dd5-104">Wenn ein Steuerelement nicht über eine eigene Caption-Eigenschaft verfügt, führen Sie die folgenden Schritte aus, um sicherzustellen, dass Barrierefreiheits Hilfen die Steuerelemente identifizieren können:</span><span class="sxs-lookup"><span data-stu-id="19dd5-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="19dd5-105">Erstellen Sie ein statisches Text Steuerelement mit einem aussagekräftigen und beschreibenden Namen.</span><span class="sxs-lookup"><span data-stu-id="19dd5-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="19dd5-106">Platzieren Sie die statische Bezeichnung, sodass Sie unmittelbar vor dem Steuerelement in der Aktivier Reihenfolge steht.</span><span class="sxs-lookup"><span data-stu-id="19dd5-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="19dd5-107">Stellen Sie sicher, dass der Bezeichnungs Text mit einem Doppelpunkt endet, z. b. "Settings:"</span><span class="sxs-lookup"><span data-stu-id="19dd5-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="19dd5-108">Positionieren Sie den Bezeichnungs Text direkt links oder vor dem Steuerelement, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="19dd5-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="19dd5-109">Machen Sie den statischen Text unsichtbar, wenn er nicht für eine visuelle Darstellung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="19dd5-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="19dd5-110">Dazu weisen Sie dem Ressourcen Skript das entsprechende Attribut zu.</span><span class="sxs-lookup"><span data-stu-id="19dd5-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="19dd5-111">Dies kann sinnvoll sein, wenn der Name oder die Funktion eines Steuer Elements mit einem anderen Mittel als statischem Text Steuerelement visuell bereitgestellt wird, z. b. eine Grafik oder ein verknüpftes Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="19dd5-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="19dd5-112">Die richtige Verwendung statischer Steuerelemente ist die einzige Möglichkeit, unterstrichene Zugriffstasten für Steuerelemente, die keine intrinsischen Bezeichnungen aufweisen, ordnungsgemäß zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="19dd5-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="19dd5-113">Weitere Informationen zur Verwendung von Steuerelementen, die keine Beschriftungs Eigenschaften aufweisen, finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="19dd5-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
