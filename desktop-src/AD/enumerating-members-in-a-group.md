---
title: Auflisten von Membern in einer Gruppe
description: Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen "Member" gespeichert.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Auflisten von Membern in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101451"
---
# <a name="enumerating-members-in-a-group"></a>Auflisten von Membern in einer Gruppe

Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen " **Member**" gespeichert. Verwenden Sie für Gruppen mit einer kleinen bis mittelgroßen Mitgliedschaft die [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) -Methode, um einen Zeiger auf ein [**iadsmembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) -Objekt zu erhalten, das die Liste aller Member enthält. Verwenden Sie dann [**iadsmembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) ein Enumeratorobjekt, das Sie zum Auflisten der Elemente verwenden können.

Wenn die erwartete Gruppenmitgliedschaft 1000 oder mehr Mitglieder sein wird, verwenden Sie den Bereich, um Benutzer jeweils einen Bereich abzurufen. Weitere Informationen zum Verwenden von Bereichen zum Auflisten von Membern finden Sie unter Auflisten von [Gruppen, die viele Member enthalten](enumerating-groups-that-contain-many-members.md).

 

 