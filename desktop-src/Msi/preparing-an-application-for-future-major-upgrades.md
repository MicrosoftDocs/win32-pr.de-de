---
description: Autoren von Installationspaketen sollten Aktualisierungsinformationen in ihre .msi-Dateien enthalten, um sicherzustellen, dass ihr Installationspaket die vollständige Upgradefunktionalität nutzen kann, die mit dem Microsoft Windows Installer verfügbar ist.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Vorbereiten einer Anwendung für zukünftige größere Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c38adc97fce578b48bc721b4265696486351097771cf936efc1e667752a7a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377351"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Vorbereiten einer Anwendung für zukünftige größere Upgrades

Autoren von Installationspaketen sollten Aktualisierungsinformationen in ihre .msi-Dateien enthalten, um sicherzustellen, dass ihr Installationspaket die vollständige Upgradefunktionalität nutzen kann, die mit dem Microsoft Windows Installer verfügbar ist.

Jeder Anwendung oder Anwendungssuite sollten eine [**UpgradeCode-Eigenschaft,**](upgradecode.md) [**eine ProductVersion-Eigenschaft**](productversion.md) und eine [**ProductLanguage-Eigenschaft zugewiesen**](productlanguage.md) werden. Die [**UpgradeCode-Eigenschaft**](upgradecode.md) gibt eine Familie verwandter Anwendungen an, die aus verschiedenen Versionen und verschiedenen Sprachversionen desselben Produkts bestehen. Weitere Informationen zur Verwendung der [**UpgradeCode-Eigenschaft**](upgradecode.md) finden Sie unter [Using an UpgradeCode](using-an-upgradecode.md).

**Vorbereiten einer Anwendung für zukünftige größere Upgrades**

1.  Bestimmen Sie einen neuen Paketcodewert für die Anwendung. Weitere Informationen zu Paketcodes finden Sie unter [Paketcodes](package-codes.md). Geben Sie den neuen Paketcode in die [**Zusammenfassungseigenschaft Revisionsnummer**](revision-number-summary.md) des [Zusammenfassungsinformationsstreams ein.](summary-information-stream.md)
2.  Bestimmen Sie eine [**neue ProductCode-Eigenschaft**](productcode.md) für die Anwendung. Weitere [Informationen finden Sie unter Ändern](changing-the-product-code.md) des Produktcodes. Geben [**Sie ProductCode**](productcode.md) und seinen Wert in die [Property-Tabelle ein.](property-table.md)
3.  Bestimmen Sie die Version der Anwendung und die [**ProductVersion-Eigenschaft.**](productversion.md) Die [**ProductVersion**](productversion.md) sollte mit jeder neuen Version der Anwendung erhöht werden. Beachten Sie, dass das Installationsprogramm nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion eingeben, ignoriert das Installationsprogramm das vierte Feld. Geben [**Sie ProductVersion**](productversion.md) und seinen Wert in die Tabelle Property ein.
4.  Bestimmen Sie die Sprache des Pakets und die [**ProductLanguage-Eigenschaft.**](productlanguage.md) Der Wert dieser Eigenschaft muss ein numerischer Sprachbezeichner (LANGID) sein. Geben [**Sie ProductLanguage**](productlanguage.md) und dessen Wert in die [Tabelle Eigenschaft ein.](property-table.md) Beachten Sie, dass [die Aktion FindRelatedProducts die](findrelatedproducts-action.md) von [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)zurückgegebene Sprache verwendet. Damit FindRelatedProducts ordnungsgemäß funktioniert, muss der Paketautor sicherstellen, dass die [**ProductLanguage-Eigenschaft**](productlanguage.md) in der Property -Tabelle auf eine Sprache festgelegt ist, die auch in der Eigenschaft Vorlagenzusammenfassung [**aufgeführt**](template-summary.md) ist.
5.  Wenn Sie ein Installationspaket für die erste Version Ihres Produkts erstellen, verwenden Sie einen neuen [**UpgradeCode.**](upgradecode.md) Wenn Ihr Paket für eine neuere Version eines vorhandenen Produkts vorgesehen ist oder die gleiche Version wie ein vorhandenes Produkt in einer anderen Sprache ist, verwenden Sie den gleichen [**UpgradeCode**](upgradecode.md) wie das vorhandene Produkt. Zwei Produkte mit derselben [**ProductVersion**](productversion.md) und derselben [**ProductLanguage**](productlanguage.md) können nicht denselben [**UpgradeCode**](upgradecode.md)haben, es sei denn, eines ist ein kleines Update [des](small-updates.md) anderen.
6.  [**UpgradeCode hat**](upgradecode.md) das Format einer [GUID.](guid.md) Geben Sie die [**UpgradeCode-GUID**](upgradecode.md) in die Tabelle Eigenschaft ein.

Weitere Informationen finden Sie unter Verhindern der Installation eines [alten Pakets über eine neuere Version.](preventing-an-old-package-from-installing-over-a-newer-version.md)

 

 



