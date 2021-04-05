---
title: Entfernen von Mitgliedern aus Gruppen in einer Domäne
description: Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Entfernen von Mitgliedern aus Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724448"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Entfernen von Mitgliedern aus Gruppen in einer Domäne

Sie können Benutzer, Gruppen oder Kontakte aus Gruppen entfernen. Das **Member** -Attribut des **Group** -Objekts enthält alle direkten Mitglieder der Gruppe.

Die einfachste Möglichkeit, ein Mitglied aus einer Gruppe zu entfernen, besteht darin, die [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) -Methode für die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle des Gruppen Objekts aufzurufen, aus dem Sie Mitglieder entfernen möchten.

 

 