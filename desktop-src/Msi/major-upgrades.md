---
description: Ein größeres Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der ProductCode-Eigenschaft erfordert.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Hauptupgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98c6364ca0a6d9622eaacdea6cd37a2cc2dd10b057405a99577acab5102f8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629156"
---
# <a name="major-upgrades"></a>Hauptupgrades

Ein größeres Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der [**ProductCode-Eigenschaft**](productcode.md) erfordert.

Bei einem typischen größeren Upgrade wird eine frühere Version einer Anwendung entfernt und eine neue Version installiert. Ein größeres Upgrade kann die Funktionskomponentenstruktur neu organisieren. Weitere Informationen finden Sie unter [**ProductCode**](productcode.md) und [Ändern des Produktcodes.](changing-the-product-code.md)

Während eines größeren Upgrades mit Windows Installer durchsucht das Installationsprogramm den Computer des Benutzers nach Anwendungen, die mit dem ausstehenden Upgrade in Zusammenhang stehen, und wenn es eines erkennt, ruft es die Version der installierten Anwendung aus der Systemregistrierung ab. Das Installationsprogramm verwendet dann Informationen in der Upgradedatenbank, um zu bestimmen, ob die installierte Anwendung aktualisiert werden soll.

Um die Upgradefunktionen des Installationsprogramms zu aktivieren, sollte jedes Paket über eine [**UpgradeCode-Eigenschaft**](upgradecode.md) und eine [Upgradetabelle verfügen.](upgrade-table.md) Jedes eigenständige Produkt oder jede eigenständige Produktsuite sollte über einen eigenen **UpgradeCode verfügen.** Weitere Informationen zur Verwendung von **UpgradeCode** finden Sie im Abschnitt [Verwenden eines UpgradeCodes.](using-an-upgradecode.md) Jeder Datensatz in der Upgradetabelle enthält eine Kombination aus Upgradecode, Produktversion und Sprachinformationen, mit denen ein Satz von Produkten identifiziert wird, die von dem Upgrade betroffen sind. Wenn die [FindRelatedProducts-Aktion](findrelatedproducts-action.md) erkennt, dass ein betroffenes Produkt auf dem System installiert ist, fügt sie den Produktcode an eine Eigenschaft in der ActionProperty -Spalte der Upgradetabelle an. Die [Aktion RemoveExistingProducts](removeexistingproducts-action.md) und die [MigrateFeatureStates-Aktion](migratefeaturestates-action.md) entfernen oder migrieren die produkte, die in der Liste ActionProperty aufgeführt sind. Paketautoren können auch das im Thema [Vorbereiten einer Anwendung für zukünftige Hauptupgrades](preparing-an-application-for-future-major-upgrades.md)beschriebene Verfahren befolgen.

Windows Installationsupgradepakete können so erstellt werden, dass keine größeren Upgrades installiert werden, wenn der Benutzer bereits eine neuere Version der Anwendung installiert hat. Weitere Informationen zum Erstellen eines Pakets, das nicht über eine neuere Version installiert wird, finden Sie unter [Verhindern der Installation eines alten Pakets über eine neuere Version.](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows Das Installationsprogramm verwendet nur die ersten drei Felder der Produktversion. Beschreibungen dieser Felder finden Sie unter [**ProductVersion-Eigenschaft.**](productversion.md) Wenn Sie ein viertes Feld in Ihre Produktversion einfügen, ignoriert das Installationsprogramm das vierte Feld.

 

Die empfohlene Methode zum Anwenden eines größeren Upgrades durch Installieren des vollständigen Pakets für das aktualisierte Produkt. Informationen zum Anwenden eines Hauptupgrades durch Installieren des Produkts finden Sie unter [Anwenden von Hauptupgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md).

Ein größeres Upgrade, das als [Patchpaket](patch-packages.md) für das Produkt angewendet wird, kann nicht mit anderen Updates sequenziert werden und ist kein [deinstallationsfähiger Patch.](uninstallable-patches.md) Informationen zum Anwenden eines Patchpakets für ein größeres Upgrade auf ein Windows Installer-Paket finden Sie unter [Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). Die Anwendung eines größeren Upgrades mithilfe eines Patchpakets wird nicht empfohlen. Wenden Sie stattdessen größere Upgrades an, indem Sie das vollständige Produkt installieren.

> [!Note]  
> Wenn eine Anwendung im [Benutzerinstallationskontext](installation-context.md)installiert wird, muss jedes größere Upgrade auf die Anwendung auch mithilfe des Benutzerkontexts durchgeführt werden. Wenn eine Anwendung im Installationskontext pro Computer installiert wird, muss jedes größere Upgrade auf die Anwendung auch mithilfe des Kontexts pro Computer durchgeführt werden. Der Windows Installer installiert keine größeren Upgrades im gesamten Installationskontext.

 

Sie können benutzerdefinierte Aktionen, die nach [InstallValidate](installvalidate-action.md) sequenziert werden, so einrichten, dass größere Upgrades mithilfe der [**UPGRADINGPRODUCTCODE-Eigenschaft**](upgradingproductcode.md) verarbeitet werden:

-   Wenn sie möchten, dass eine benutzerdefinierte Aktion während einer Deinstallation des Produkts ausgeführt wird, aber nicht während der Entfernung des Produkts durch ein größeres Upgrade, verwenden Sie diese Bedingung.

    REMOVE="ALL" AND NOT [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Wenn eine benutzerdefinierte Aktion nur während eines größeren Upgrades ausgeführt werden soll, verwenden Sie diese Bedingung.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



