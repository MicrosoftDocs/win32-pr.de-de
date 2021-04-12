---
description: Bevor das Smartcardsubsystem eine Smartcard finden kann, muss die Smartcard in das System eingefügt werden.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Einführung in Smartcards für das System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217766"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="a66d2-103">Einführung in Smartcards für das System</span><span class="sxs-lookup"><span data-stu-id="a66d2-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="a66d2-104">Bevor das [*Smartcardsubsystem*](../secgloss/s-gly.md) eine [*Smartcard*](../secgloss/s-gly.md)finden kann, muss die Smartcard in das System eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a66d2-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="a66d2-105">Dies erfolgt in der Regel mit einem Smartcard-Setup Tool, das vom Kartenhersteller bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a66d2-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="a66d2-106">Das Tool könnte als Programm auf einer Diskette (mit der Smartcard), einem ActiveX-Steuerelement, das auf einer Website verfügbar ist, usw. stehen.</span><span class="sxs-lookup"><span data-stu-id="a66d2-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="a66d2-107">Das Setup Tool muss die folgenden Informationen zur Karte bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="a66d2-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="a66d2-108">Die [*ATR-Zeichenfolge*](../secgloss/a-gly.md)und eine optionale Maske, die als Hilfe bei der Identifizierung der Karte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a66d2-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="a66d2-109">Eine Liste der smartcardschnittstellen, die von der Karte unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a66d2-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="a66d2-110">Ein Anzeige Name für die Karte, der zum Identifizieren der Karte für den Benutzer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a66d2-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="a66d2-111">In den meisten Fällen wird dies vom Benutzer für das Setup-Tool bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a66d2-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="a66d2-112">Der [*primäre Dienstanbieter*](../secgloss/p-gly.md) , der der Karte (optional) zugeordnet ist und für den Zugriff auf die Karte über COM-Schnittstellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a66d2-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="a66d2-113">Zum Vereinfachen der Setup Tools und zur Gewährleistung der Integrität der [*smartcarddatenbank*](../secgloss/s-gly.md)bietet das Smartcard-Subsystem die folgenden zwei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a66d2-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="a66d2-114">Mit " [**scardintroducecardtype**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) " wird eine Smartcard in die Datenbank eingeführt, und " [**scardforgetcardtype**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) " wird aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="a66d2-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
