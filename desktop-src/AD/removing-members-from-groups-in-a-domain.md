---
title: Entfernen von Mitgliedern aus Gruppen in einer Domäne
description: Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- gruppen AD , Entfernen von Mitgliedern aus Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025158"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Entfernen von Mitgliedern aus Gruppen in einer Domäne

Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen. Das  Memberattribut des **Gruppenobjekts** enthält alle direkten Mitglieder der Gruppe.

Die einfachste Möglichkeit, ein Element aus einer Gruppe zu entfernen, besteht darin, die [**IADsGroup.Remove-Methode**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) auf der [**IADsGroup-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsgroup) des Gruppenobjekts aufzurufen, aus dem Sie Member entfernen möchten.

 

 