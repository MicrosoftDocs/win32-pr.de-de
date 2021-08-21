---
title: Die SetInfo-Methode
description: Die SetInfo-Methode der IADs speichert die aktuellen Werte für die Eigenschaften für dieses Active Directory-Objekt aus dem Eigenschaftencache im zugrunde liegenden Verzeichnisspeicher. Dies entspricht dem Leeren eines Puffers auf den Datenträger.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI mit
- 'ADSI-Eigenschaften: Speichern Sie die aktuellen Werte für Eigenschaften.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023138"
---
# <a name="the-setinfo-method"></a>Die SetInfo-Methode

Die [**IADs::SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) speichert die aktuellen Werte für die Eigenschaften für dieses Active Directory-Objekt aus dem Eigenschaftencache im zugrunde liegenden Verzeichnisspeicher. Dies entspricht dem Leeren eines Puffers auf den Datenträger.

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aktualisiert Objekte, die bereits im Verzeichnis vorhanden sind, oder erstellt einen neuen Verzeichniseintrag für neu erstellte Objekte.

Wenn zum Zeitpunkt des [**SetInfo-Aufrufs**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Eigenschaftscachewerte mit einem [**PutEx-Steuerelementcode**](/windows/desktop/api/Iads/nf-iads-iads-putex) wie ADS PROPERTY UPDATE oder ADS PROPERTY CLEAR geschrieben \_ \_ \_ \_ wurden, werden die entsprechenden Anforderungen an den zugrunde liegenden Verzeichnisdienst übergeben.

 

 




