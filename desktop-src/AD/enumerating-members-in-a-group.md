---
title: Aufzählen von Mitgliedern in einer Gruppe
description: Erfahren Sie mehr über das Aufzählen von Mitgliedern in Azure Active Directory Gruppe. Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens member gespeichert.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Aufzählen von Mitgliedern in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426e2fb4fdd47f5f5b277618cb0989d8d8b06b6491d505ece20139e373ebe01f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429485"
---
# <a name="enumerating-members-in-a-group"></a>Aufzählen von Mitgliedern in einer Gruppe

Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens Member **gespeichert.** Verwenden Sie für Gruppen mit einer kleinen bis mittelgroßen Mitgliedschaft die [**IADsGroup.Members-Methode,**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) um einen Zeiger auf ein [**IADsMembers-Objekt**](/windows/desktop/api/iads/nn-iads-iadsmembers) zu erhalten, das die Liste aller Mitglieder enthält. Verwenden Sie dann [**IADsMembers::get \_ \_ NewEnum,**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) um ein Enumeratorobjekt zu erhalten, mit dem Sie die Member aufzählen können.

Wenn die erwartete Gruppenmitgliedschaft 1.000 oder mehr Mitglieder beträgt, verwenden Sie range, um Benutzer nach einem Bereich abzurufen. Weitere Informationen zur Verwendung von im Bereich zum Aufzählen von Membern finden Sie unter Aufzählen von Gruppen, [die viele Elemente enthalten.](enumerating-groups-that-contain-many-members.md)

 

 