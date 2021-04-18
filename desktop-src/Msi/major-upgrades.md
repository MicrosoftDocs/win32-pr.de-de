---
description: Ein großes Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der Eigenschaft ProductCode erfordert.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Wichtige Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527032"
---
# <a name="major-upgrades"></a>Wichtige Upgrades

Ein großes Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der Eigenschaft [**ProductCode**](productcode.md) erfordert.

Bei einem typischen Haupt Upgrade wird eine frühere Version einer Anwendung entfernt, und es wird eine neue Version installiert. Ein großes Upgrade kann die Funktionskomponenten Struktur neu organisieren. Weitere Informationen finden Sie unter [**ProductCode**](productcode.md) und [Ändern des Produktcodes](changing-the-product-code.md).

Während eines größeren Upgrades mithilfe von Windows Installer durchsucht das Installationsprogramm den Computer des Benutzers nach Anwendungen, die sich auf das ausstehende Upgrade beziehen. wenn es erkannt wird, wird die Version der installierten Anwendung aus der Systemregistrierung abgerufen. Der Installer verwendet dann Informationen in der upgradedatenbank, um zu bestimmen, ob die installierte Anwendung aktualisiert werden soll.

Zum Aktivieren der upgradefunktionen des Installers sollte jedes Paket über eine [**UpgradeCode**](upgradecode.md) -Eigenschaft und eine [upgradetabelle](upgrade-table.md)verfügen. Jedes eigenständige Produkt oder jede Produktsuite sollte über einen eigenen **UpgradeCode** verfügen. Weitere Informationen zur Verwendung von **UpgradeCode** finden Sie im Abschnitt [Verwenden von UpgradeCode](using-an-upgradecode.md). Jeder Datensatz in der upgradetabelle bietet eine Kombination aus dem UpgradeCode, der Produktversion und den Sprachinformationen, die verwendet werden, um eine Gruppe von Produkten zu identifizieren, die vom Upgrade betroffen sind. Wenn die [Aktion "FindRelatedProducts](findrelatedproducts-action.md) " erkennt, dass ein betroffenes Produkt auf dem System installiert ist, fügt Sie den Produktcode an eine Eigenschaft in der Spalte "action Property" der upgradetabelle an. Mit der [Aktion "RemoveExistingProducts](removeexistingproducts-action.md) " und der [MigrateFeatureStates-Aktion](migratefeaturestates-action.md) werden die in der Liste "action Property" aufgeführten Produkte entfernt oder migriert. Paket Ersteller können auch das Verfahren befolgen, das im Thema: [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)beschrieben wird.

Windows Installer Upgradepakete können so erstellt werden, dass größere Upgrades nicht installiert werden, wenn der Benutzer bereits eine neuere Version der Anwendung installiert hat. Weitere Informationen zum Erstellen eines Pakets, das nicht über eine neuere Version installiert wird, finden Sie unter [verhindern, dass ein altes Paket über eine neuere Version installiert](preventing-an-old-package-from-installing-over-a-newer-version.md) wird.

> [!Note]  
> Windows Installer verwendet nur die ersten drei Felder der Produktversion. Beschreibungen dieser Felder finden Sie unter der [**ProductVersion**](productversion.md) -Eigenschaft. Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert.

 

Die empfohlene Methode für das Anwenden eines größeren Upgrades durch Installieren des vollständigen Pakets für das aktualisierte Produkt. Informationen zum Anwenden eines größeren Upgrades durch die Installation des Produkts finden Sie unter [Anwenden von größeren Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md).

Ein umfangreiches Upgrade, das als [Patchpaket](patch-packages.md) für das Produkt angewendet wird, kann nicht mit anderen Updates sequenziert werden und ist kein nicht [installier barer Patch](uninstallable-patches.md). Informationen zum Anwenden eines wichtigen Upgradepatch-Pakets auf ein Windows Installer Paket finden Sie unter [Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). Die Anwendung eines größeren Upgrades mithilfe eines Patch-Pakets wird nicht empfohlen. wenden Sie stattdessen größere Upgrades an, indem Sie das vollständige Produkt installieren.

> [!Note]  
> Wenn eine Anwendung im [Installations Kontext](installation-context.md)pro Benutzer installiert wird, müssen alle wichtigen Upgrades der Anwendung auch über den Kontext pro Benutzer ausgeführt werden. Wenn eine Anwendung im computerspezifischen Installations Kontext installiert wird, muss jedes wesentliche Upgrade auf die Anwendung auch über den computerspezifischen Kontext durchgeführt werden. Bei der Windows Installer werden wichtige Upgrades nicht über den Installations Kontext hinweg installiert.

 

Sie können benutzerdefinierte Aktionen, die nach [InstallValidate](installvalidate-action.md) sequenziert werden, für die Verarbeitung großer Upgrades mithilfe der [**upgradingproductcode**](upgradingproductcode.md) -Eigenschaft bedinieren:

-   Wenn eine benutzerdefinierte Aktion während der Deinstallation des Produkts, aber nicht während des Entfernens des Produkts durch ein großes Upgrade ausgeführt werden soll, verwenden Sie diese Bedingung.

    Remove = "All" und nicht [ **upgradingproductcode**](upgradingproductcode.md)

-   Wenn Sie möchten, dass eine benutzerdefinierte Aktion nur während eines größeren Upgrades ausgeführt wird, verwenden Sie diese Bedingung.

    [**Upgradingproductcode**](upgradingproductcode.md)

 

 



