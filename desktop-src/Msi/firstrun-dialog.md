---
description: In einer Reihenfolge von FIRSTRUN-Dialogfeldern werden Benutzername, Firmenname und Produkt-ID-Informationen erfasst. Das Installationsprogramm überprüft die Produkt-ID in diesem Dialogfeld.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Dialog Feld "FIRSTRUN"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215124"
---
# <a name="firstrun-dialog"></a>Dialog Feld "FIRSTRUN"

In einer Reihenfolge von FIRSTRUN-Dialogfeldern werden Benutzername, Firmenname und Produkt-ID-Informationen erfasst. Das Installationsprogramm überprüft die Produkt-ID in diesem Dialogfeld.

Eine FIRSTRUN-Dialogfeld Sequenz ist in der Regel kein Teil der Aktions Sequenz und wird stattdessen von der [**msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) -Funktion bei der ersten Produktführung aufgerufen.

Ein Autor eines Installer-Pakets kann die Vorlagen dialogsequenz verwenden oder eine andere Sequenz erstellen. Die Dialog Sequenz erfordert jedoch, dass der Benutzer die folgenden Eigenschaften festgelegt hat:

-   [**Username**](username.md) -Eigenschaft
-   [**CompanyName**](companyname.md) -Eigenschaft
-   [**PIDKEY**](pidkey.md) (Eigenschaft)

Die Produkt-ID wird während des Dialog Felds mit der [ValidateProductID-Aktion](validateproductid-action.md) oder dem [ValidateProductID-ControlEvent](validateproductid-controlevent.md)überprüft.

Wenn die Produkt-ID als Eigenschaft in der Befehlszeile oder durch eine Transformation festgelegt wird, kann die Notwendigkeit, dass der Benutzer die Produkt-ID während des ersten Testlaufs erneut eingeben muss, umgangen werden, indem die Anzeige mithilfe der [**ProductID**](productid.md) -Eigenschaft gesteuert wird. Nach der erfolgreichen Überprüfung der Produkt-ID wird die **ProductID-** Eigenschaft auf die vollständige, gültige Produkt-ID festgelegt.

 

 



