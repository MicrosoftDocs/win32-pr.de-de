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
# <a name="the-setinfo-method"></a>Die Methode "* tinfo"

Die [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode speichert die aktuellen Werte für die Eigenschaften dieses Active Directory Objekts aus dem Eigenschafts Cache in den zugrunde liegenden Verzeichnis Speicher. Dies ist analog zum leeren eines Puffers auf den Datenträger.

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aktualisiert Objekte, die bereits im Verzeichnis vorhanden sind, oder erstellt einen neuen Verzeichniseintrag für neu erstellte Objekte.

Zum Zeitpunkt des [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Aufrufs wurden [](/windows/desktop/api/Iads/nf-iads-iads-putex) \_ \_ \_ \_ die entsprechenden Anforderungen an den zugrunde liegenden Verzeichnisdienst weitergeleitet, wenn Eigenschafts Cache Werte mit einem PutEx-Steuerungs Code geschrieben wurden, z. b. ADS-Eigenschafts Update oder ADS-Eigenschaft clear.

 

 




