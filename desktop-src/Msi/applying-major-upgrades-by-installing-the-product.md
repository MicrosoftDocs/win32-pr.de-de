---
description: Ein großes Upgrade kann durch Installieren des neuen Installationspakets für das aktualisierte Produkt angewendet werden.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Anwenden von größeren Upgrades durch Installieren des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347123"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Anwenden von größeren Upgrades durch Installieren des Produkts

Ein großes Upgrade kann durch Installieren des neuen Installationspakets für das aktualisierte Produkt angewendet werden. Da größere Upgrades einen anderen Produktcode als das ursprüngliche Produkt erhalten, muss die Installation des Upgrades als Installation eines neuen Produkts behandelt werden. Das Upgrade kann einfach wie ein anderes Produkt installiert werden. Das neue Installationspaket kann das Entfernen des alten Produkts durch einschließen der [upgradetabelle](upgrade-table.md) und der Aktion [FindRelatedProducts](findrelatedproducts-action.md) und [RemoveExistingProducts](removeexistingproducts-action.md)verarbeiten.

**So verteilen Sie ein großes Upgrade an aktuelle Benutzer über die Befehlszeile**

-   Verwenden Sie in der Befehlszeile: **msiexec/i \[** _path to aktualisierte msi file_*_\]_*

**So verteilen Sie ein großes Upgrade an aktuelle Benutzer von einem Programm**

-   Geben Sie in einem Programm [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ein, und geben Sie den Pfad zur aktualisierten MSI-Datei an.

 

 



