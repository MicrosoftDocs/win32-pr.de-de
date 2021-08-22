---
description: In der Dialogfeldsequenz FirstRun werden Informationen zu Benutzername, Unternehmensname und Produkt-ID gesammelt. Das Installationsprogramm überprüft die Produkt-ID während dieses Dialogfelds.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: FirstRun-Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de44417014aefb84d2d381166d5a2fceb7f956c4212e9dba31556053c583fef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828890"
---
# <a name="firstrun-dialog"></a>FirstRun-Dialogfeld

In der Dialogfeldsequenz FirstRun werden Informationen zu Benutzername, Unternehmensname und Produkt-ID gesammelt. Das Installationsprogramm überprüft die Produkt-ID während dieses Dialogfelds.

Eine FirstRun-Dialogfeldsequenz ist in der Regel kein Teil der Aktionssequenz und wird stattdessen von der [**MsiCollectUserInfo-Funktion**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) bei der ersten Ausführung des Produkts aufgerufen.

Ein Autor eines Installationspakets kann die Vorlagendialogsequenz verwenden oder eine andere Sequenz erstellen. Für die Dialogsequenz muss der Benutzer jedoch die folgenden Eigenschaften festlegen:

-   [**USERNAME-Eigenschaft**](username.md)
-   [**COMPANYNAME-Eigenschaft**](companyname.md)
-   [**PIDKEY-Eigenschaft**](pidkey.md)

Die Produkt-ID wird während des Dialogs mit der [ValidateProductID-Aktion](validateproductid-action.md) oder dem [ValidateProductID ControlEvent überprüft.](validateproductid-controlevent.md)

Wenn die Produkt-ID als Eigenschaft in der Befehlszeile oder durch eine Transformation festgelegt wird, kann die Notwendigkeit, dass der Benutzer die Produkt-ID während des Dialogfelds für die erste Ausführung erneut eingeht, umgangen werden, indem die Anzeige mithilfe der [**ProductID-Eigenschaft**](productid.md) kontrolliert wird. Nach der erfolgreichen Überprüfung der Produkt-ID wird die **ProductID-Eigenschaft** auf die vollständige, gültige Produkt-ID festgelegt.

 

 



