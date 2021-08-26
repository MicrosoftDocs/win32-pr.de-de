---
description: Ein größeres Upgrade kann angewendet werden, indem das neue Installationspaket für das aktualisierte Produkt installiert wird.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Anwenden wichtiger Upgrades durch Installieren des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79570051ddbff27b12a11e04e41c37f4babad96ff045bc408e00c2b7164b263a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045680"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Anwenden wichtiger Upgrades durch Installieren des Produkts

Ein größeres Upgrade kann angewendet werden, indem das neue Installationspaket für das aktualisierte Produkt installiert wird. Da größere Upgrades einen anderen Produktcode als das ursprüngliche Produkt erhalten, muss die Installation des Upgrades als Installation eines neuen Produkts behandelt werden. Das Upgrade kann einfach wie ein anderes Produkt installiert werden. Sie können das neue Installationspaket das Entfernen des alten Produkts übernehmen, indem Sie die [Tabelle Upgrade](upgrade-table.md) und die [Aktion FindRelatedProducts](findrelatedproducts-action.md) und [die Aktion RemoveExistingProducts](removeexistingproducts-action.md)einschließen.

**So propagieren Sie ein größeres Upgrade über die Befehlszeile an aktuelle Benutzer**

-   Verwenden Sie in der Befehlszeile: msiexec /i path to updated msi file (msiexec **/i-Pfad \[** _zur aktualisierten MSI-Datei)._*_\]_*

**So wird ein größeres Upgrade von einem Programm an aktuelle Benutzer weiter verbreitet**

-   Rufen Sie in einem Programm [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) auf, und geben Sie den Pfad zur aktualisierten MSI-Datei an.

 

 



