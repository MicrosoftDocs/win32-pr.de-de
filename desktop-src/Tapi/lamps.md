---
description: Die Lampen auf einem Telefongerät können in einer Vielzahl verschiedener beleuchtungsmodi beleuchtet werden.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Aufleuchten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050310"
---
# <a name="lamps"></a><span data-ttu-id="bc343-103">Aufleuchten</span><span class="sxs-lookup"><span data-stu-id="bc343-103">Lamps</span></span>

<span data-ttu-id="bc343-104">Die Lampen auf einem Telefongerät können in einer Vielzahl verschiedener beleuchtungsmodi beleuchtet werden.</span><span class="sxs-lookup"><span data-stu-id="bc343-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="bc343-105">Im Gegensatz zu klingeln Mustern sind Lamp-Modi in Telefon Sätzen verschiedener Lieferanten eher einheitlich.</span><span class="sxs-lookup"><span data-stu-id="bc343-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="bc343-106">Eine gemeinsame Gruppe von LAMP-Modi wird von der-API definiert.</span><span class="sxs-lookup"><span data-stu-id="bc343-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="bc343-107">Eine von der Lamp-Schaltflächen-ID identifizierte Lamp kann in einem bestimmten Lamp-Modus beleuchtet werden.</span><span class="sxs-lookup"><span data-stu-id="bc343-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="bc343-108">Eine Lamp kann auch für den aktuellen Lamp-Modus abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="bc343-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="bc343-109">Die für die-Leuchten verwendeten TAPI-Funktionen sind [**phonesetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), das eine LAMP auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lamp-Beleuchtungs Modus und [**phonegetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), das den aktuellen Lamp-Modus der angegebenen Lamp zurückgibt, beleuchtet.</span><span class="sxs-lookup"><span data-stu-id="bc343-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="bc343-110">Wenn eine Lamp-Anlage eines Mobiltelefons geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="bc343-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="bc343-111">Die Parameter für diese Nachricht geben Aufschluss über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="bc343-111">Parameters to this message provide an indication of the change.</span></span>

 

 



