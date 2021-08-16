---
description: Ein umfangreiches Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der ProductCode-Eigenschaft benötigt.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Wichtige Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98c6364ca0a6d9622eaacdea6cd37a2cc2dd10b057405a99577acab5102f8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629156"
---
# <a name="major-upgrades"></a>Wichtige Upgrades

Ein umfangreiches Upgrade ist ein umfassendes Update eines Produkts, das eine Änderung der [**ProductCode-Eigenschaft**](productcode.md) benötigt.

Bei einem typischen Hauptupgrade wird eine frühere Version einer Anwendung entfernt und eine neue Version installiert. Bei einem größeren Upgrade kann die Funktionskomponentenstruktur neu organisiert werden. Weitere Informationen finden Sie unter [**ProductCode**](productcode.md) und [Ändern des Produktcodes.](changing-the-product-code.md)

Während eines größeren Upgrades mithilfe des Windows-Installers durchsucht das Installationsprogramm den Computer des Benutzers nach Anwendungen, die mit dem ausstehenden Upgrade in Verbindung stehen, und wenn es eines erkennt, ruft es die Version der installierten Anwendung aus der Systemregistrierung ab. Das Installationsprogramm verwendet dann Informationen in der Upgradedatenbank, um zu bestimmen, ob die installierte Anwendung aktualisiert werden soll.

Um die Upgradefunktionen des Installationsprogramms zu aktivieren, muss jedes Paket über eine [**UpgradeCode-Eigenschaft**](upgradecode.md) und eine [Upgradetabelle verfügen.](upgrade-table.md) Jedes eigenständige Produkt oder jede eigenständige Produktsuite sollte über einen eigenen **UpgradeCode verfügen.** Weitere Informationen zur Verwendung von **UpgradeCode finden Sie** im Abschnitt [Verwenden eines UpgradeCodes.](using-an-upgradecode.md) Jeder Datensatz in der Upgradetabelle enthält eine Kombination aus Upgradecode, Produktversion und Sprachinformationen, die verwendet werden, um eine Gruppe von Produkten zu identifizieren, die vom Upgrade betroffen sind. Wenn die [Aktion FindRelatedProducts](findrelatedproducts-action.md) erkennt, dass ein betroffenes Produkt auf dem System installiert ist, fügt sie den Produktcode an eine Eigenschaft in der Spalte ActionProperty der Tabelle Upgrade an. Mit [der RemoveExistingProducts-Aktion](removeexistingproducts-action.md) und der [MigrateFeatureStates-Aktion](migratefeaturestates-action.md) werden die in der Liste ActionProperty aufgeführten Produkte entfernt oder migriert. Paketautoren können auch das im Thema Vorbereiten einer Anwendung für zukünftige Hauptupgrades [beschriebene Verfahren befolgen.](preparing-an-application-for-future-major-upgrades.md)

Windows Installationsupgradepakete können so verfasst werden, dass größere Upgrades nicht installiert werden, wenn der Benutzer bereits eine neuere Version der Anwendung installiert hat. Weitere Informationen zum Erstellen eines Pakets, das nicht über eine neuere Version installiert wird, finden Sie unter Verhindern der Installation eines alten Pakets über eine [neuere Version.](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows Das Installationsprogramm verwendet nur die ersten drei Felder der Produktversion. Beschreibungen dieser Felder finden Sie unter [**ProductVersion-Eigenschaft.**](productversion.md) Wenn Sie ein viertes Feld in Ihre Produktversion eingeben, ignoriert das Installationsprogramm das vierte Feld.

 

Die empfohlene Methode zum Anwenden eines größeren Upgrades durch Installieren des vollständigen Pakets für das aktualisierte Produkt. Informationen zum Anwenden eines größeren Upgrades durch Installieren des Produkts finden Sie unter [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).

Ein größeres Upgrade, das als [Patchpaket für](patch-packages.md) das Produkt angewendet wird, kann nicht mit anderen Updates sequenziert werden und ist kein [deinstallationsfähiger Patch.](uninstallable-patches.md) Informationen zum Anwenden eines größeren Upgradepatchpakets auf ein Windows Installer-Paket finden Sie unter Applying [Major Upgrades by Patching the Local Installation of the Product](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). Die Anwendung eines größeren Upgrades mithilfe eines Patchpakets wird nicht empfohlen. Wenden Sie stattdessen größere Upgrades an, indem Sie das vollständige Produkt installieren.

> [!Note]  
> Wenn eine Anwendung im Benutzerinstallationskontext installiert [wird,](installation-context.md)muss jedes größere Upgrade der Anwendung auch im Benutzerkontext ausgeführt werden. Wenn eine Anwendung im Installationskontext pro Computer installiert wird, muss jedes größere Upgrade der Anwendung auch mit dem Computerkontext ausgeführt werden. Der Windows Installer installiert keine größeren Upgrades im installationskontextübergreifenden Kontext.

 

Sie können benutzerdefinierte Aktionen, die nach [InstallValidate](installvalidate-action.md) sequenziert werden, zur Handhabung wichtiger Upgrades mithilfe der [**UPGRADINGPRODUCTCODE-Eigenschaft bedingungsdefiniert**](upgradingproductcode.md) machen:

-   Wenn sie möchten, dass eine benutzerdefinierte Aktion während einer Deinstallation des Produkts, aber nicht während der Entfernung des Produkts durch ein größeres Upgrade ausgeführt wird, verwenden Sie diese Bedingung.

    REMOVE="ALL" AND NOT [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Wenn eine benutzerdefinierte Aktion nur während eines größeren Upgrades ausgeführt werden soll, verwenden Sie diese Bedingung.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



