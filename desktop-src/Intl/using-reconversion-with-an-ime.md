---
description: Ein IME implementiert eine Funktion mit dem Namen &\# 0034; Neukonvertierung&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Verwenden der erneuten Konvertierung mit einem IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340144"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="3b011-103">Verwenden der erneuten Konvertierung mit einem IME</span><span class="sxs-lookup"><span data-stu-id="3b011-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="3b011-104">Ein IME implementiert eine Funktion namens "Reconversion".</span><span class="sxs-lookup"><span data-stu-id="3b011-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="3b011-105">Normalerweise bestimmt der imm die Listen der Kandidaten nur auf der Grundlage von Einträgen, die vom Benutzer eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="3b011-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="3b011-106">Die erneute Konvertierung ermöglicht dem imm, eine oder mehrere Kandidaten basierend auf dem enthaltenden Satz (dem Kontext) zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3b011-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="3b011-107">Die definierten neukonvertierungs Typen sind einfach, normal und erweitert.</span><span class="sxs-lookup"><span data-stu-id="3b011-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="3b011-108">Eine erneute Konvertierung ist nützlich, wenn ein Benutzer einen Kompositions Fehler in einem Dokument bemerkt.</span><span class="sxs-lookup"><span data-stu-id="3b011-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="3b011-109">Der Benutzer kann den Fehler auswählen und in einem Menü neu konvertieren auswählen.</span><span class="sxs-lookup"><span data-stu-id="3b011-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="3b011-110">Der IME verwendet den Kontext, um die beste Ersetzung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3b011-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="3b011-111">Die Anwendung kann " [**immsetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) " verwenden, um die erneute Konvertierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3b011-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b011-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b011-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b011-113">Verwenden des Eingabemethoden-Managers</span><span class="sxs-lookup"><span data-stu-id="3b011-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



