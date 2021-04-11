---
title: Transaktionsflags
description: Ein-Objekt kann entweder im direkten oder im transaktiven Modus geöffnet werden.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206928"
---
# <a name="transaction-flags"></a><span data-ttu-id="fd53f-103">Transaktionsflags</span><span class="sxs-lookup"><span data-stu-id="fd53f-103">Transaction Flags</span></span>

<span data-ttu-id="fd53f-104">Ein-Objekt kann entweder im direkten oder im transaktiven Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="fd53f-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="fd53f-105">Wenn ein Objekt im direkten Modus geöffnet wird, werden die Änderungen sofort und dauerhaft vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="fd53f-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="fd53f-106">Wenn ein Objekt im transaktiven Modus geöffnet wird, werden die Änderungen gepuffert, sodass Sie nach Abschluss der Bearbeitung explizit committet oder wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="fd53f-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="fd53f-107">Geänderte Änderungen werden im-Objekt gespeichert, während wiederhergestellte Änderungen verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="fd53f-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="fd53f-108">Der direkte Modus ist der Standard Zugriffsmodus.</span><span class="sxs-lookup"><span data-stu-id="fd53f-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="fd53f-109">Der transaktive Modus ist auf einem übergeordneten Speicher Objekt nicht erforderlich, um ihn für ein untergeordnetes Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd53f-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="fd53f-110">Eine Transaktion für ein geschachteltes Element ist jedoch innerhalb der Transaktion für das übergeordnete Speicher Objekt geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="fd53f-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="fd53f-111">Daher kann für Änderungen, die an einem untergeordneten Objekt vorgenommen werden, erst dann ein Commit ausgeführt werden, wenn für das übergeordnete Objekt ein Commit ausgeführt wurde und für beide ein Commit ausgeführt wird, bis das Stamm Speicher Objekt (das übergeordnete Element der obersten Ebene) tatsächlich auf den</span><span class="sxs-lookup"><span data-stu-id="fd53f-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="fd53f-112">Anders ausgedrückt: die Änderungen werden nach außen verschoben: innere Objekte veröffentlichen Änderungen an den Transaktionen ihrer unmittelbaren Container.</span><span class="sxs-lookup"><span data-stu-id="fd53f-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




