---
title: Die Methode "* tinfo"
description: Die IADs SetInfo-Methode speichert die aktuellen Werte für die Eigenschaften dieses Active Directory Objekts aus dem Eigenschafts Cache in den zugrunde liegenden Verzeichnis Speicher. Dies ist analog zum leeren eines Puffers auf den Datenträger.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- "\"Ttinfo ADSI\", Verwendung von"
- Eigenschaften ADSI, Speichern der aktuellen Werte für Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309215"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="9bde1-106">Die Methode "\* tinfo"</span><span class="sxs-lookup"><span data-stu-id="9bde1-106">The SetInfo Method</span></span>

<span data-ttu-id="9bde1-107">Die [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode speichert die aktuellen Werte für die Eigenschaften dieses Active Directory Objekts aus dem Eigenschafts Cache in den zugrunde liegenden Verzeichnis Speicher.</span><span class="sxs-lookup"><span data-stu-id="9bde1-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="9bde1-108">Dies ist analog zum leeren eines Puffers auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9bde1-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="9bde1-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aktualisiert Objekte, die bereits im Verzeichnis vorhanden sind, oder erstellt einen neuen Verzeichniseintrag für neu erstellte Objekte.</span><span class="sxs-lookup"><span data-stu-id="9bde1-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="9bde1-110">Zum Zeitpunkt des [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Aufrufs wurden [](/windows/desktop/api/Iads/nf-iads-iads-putex) \_ \_ \_ \_ die entsprechenden Anforderungen an den zugrunde liegenden Verzeichnisdienst weitergeleitet, wenn Eigenschafts Cache Werte mit einem PutEx-Steuerungs Code geschrieben wurden, z. b. ADS-Eigenschafts Update oder ADS-Eigenschaft clear.</span><span class="sxs-lookup"><span data-stu-id="9bde1-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




