---
description: Sitzungsschlüssel sind Schlüssel, die generiert werden, damit Sie in einer einzelnen Kommunikationssitzung verwendet werden können.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Sitzungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369808"
---
# <a name="session-keys"></a><span data-ttu-id="85840-103">Sitzungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="85840-103">Session Keys</span></span>

<span data-ttu-id="85840-104">[*Sitzungsschlüssel*](../secgloss/s-gly.md) sind Schlüssel, die generiert werden, damit Sie in einer einzelnen Kommunikationssitzung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="85840-104">[*Session keys*](../secgloss/s-gly.md) are keys that are generated to be used in a single communication session.</span></span> <span data-ttu-id="85840-105">Sitzungsschlüssel werden häufig geändert und verworfen, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="85840-105">Session keys are frequently changed and are discarded when they are no longer needed.</span></span> <span data-ttu-id="85840-106">TLS verwendet beispielsweise für jede Verbindung einen separaten Sitzungsschlüssel, und S/MIME verwendet für jede e-Mail-Nachricht einen separaten Sitzungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="85840-106">For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message.</span></span> <span data-ttu-id="85840-107">In der Regel wird ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) als Sitzungsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="85840-107">Typically a [*symmetric key*](../secgloss/s-gly.md) is used as the session key.</span></span>

<span data-ttu-id="85840-108">Sitzungsschlüssel sind flüchtig.</span><span class="sxs-lookup"><span data-stu-id="85840-108">Session keys are volatile.</span></span> <span data-ttu-id="85840-109">Anwendungen können diese Schlüssel zur späteren Verwendung oder zur Übertragung an andere Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="85840-109">Applications can save these keys for later use or for transmission to other users.</span></span> <span data-ttu-id="85840-110">Weitere Informationen finden Sie unter [kryptografieschlüsselspeicher und Exchange](cryptographic-key-storage-and-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="85840-110">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).</span></span>

 

 
