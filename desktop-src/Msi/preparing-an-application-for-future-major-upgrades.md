---
description: Autoren von Installationspaketen sollten Upgradeinformationen in ihren MSI-Dateien enthalten, um sicherzustellen, dass das Installationspaket von der vollständigen upgradefunktionalität profitieren kann, die mit dem Microsoft Windows Installer verfügbar ist.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Vorbereiten einer Anwendung für zukünftige größere Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dc9ccbee10becc39274e91d2fedeb3707028
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347119"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Vorbereiten einer Anwendung für zukünftige größere Upgrades

Autoren von Installationspaketen sollten Upgradeinformationen in ihren MSI-Dateien enthalten, um sicherzustellen, dass das Installationspaket von der vollständigen upgradefunktionalität profitieren kann, die mit dem Microsoft Windows Installer verfügbar ist.

Jeder Anwendung oder Suite von Anwendungen sollten eine [**UpgradeCode**](upgradecode.md) -Eigenschaft, eine [**ProductVersion**](productversion.md) -Eigenschaft und eine [**productlanguage**](productlanguage.md) -Eigenschaft zugewiesen werden. Die [**UpgradeCode**](upgradecode.md) -Eigenschaft gibt eine Familie Verwandter Anwendungen an, die aus verschiedenen Versionen und verschiedenen Sprachversionen desselben Produkts bestehen. Weitere Informationen zum Verwenden der [**UpgradeCode**](upgradecode.md) -Eigenschaft finden Sie unter [Verwenden von UpgradeCode](using-an-upgradecode.md).

**Vorbereiten einer Anwendung für zukünftige größere Upgrades**

1.  Bestimmen Sie einen neuen Paket Codewert für die Anwendung. Weitere Informationen zu Paket Codes finden Sie unter [Paket Codes](package-codes.md). Geben Sie den neuen Paketcode in die [**Zusammenfassungs Eigenschaft Revisionsnummer**](revision-number-summary.md) des [Datenstroms für die Zusammenfassungs Informationen](summary-information-stream.md)ein.
2.  Legen Sie eine neue [**ProductCode**](productcode.md) -Eigenschaft für die Anwendung fest. Weitere Informationen finden Sie [unter Ändern des Produktcodes](changing-the-product-code.md) . Geben Sie [**ProductCode**](productcode.md) und seinen Wert in die [Eigenschaften Tabelle](property-table.md)ein.
3.  Bestimmen Sie die Version der Anwendung und die [**ProductVersion**](productversion.md) -Eigenschaft. Die [**ProductVersion**](productversion.md) sollte sich mit jeder neuen Version der Anwendung erhöhen. Beachten Sie, dass das Installationsprogramm nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert. Geben Sie [**ProductVersion**](productversion.md) und deren Wert in die Eigenschaften Tabelle ein.
4.  Bestimmen Sie die Sprache des Pakets und die [**productlanguage**](productlanguage.md) -Eigenschaft. Der Wert dieser Eigenschaft muss eine numerische sprach Kennung (langid) sein. Geben Sie [**productlanguage**](productlanguage.md) und deren Wert in die [Eigenschaften Tabelle](property-table.md)ein. Beachten Sie, dass die [FindRelatedProducts-Aktion](findrelatedproducts-action.md) die von [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)zurückgegebene Sprache verwendet. Damit FindRelatedProducts ordnungsgemäß funktioniert, muss der Paket Ersteller sicherstellen, dass die [**productlanguage**](productlanguage.md) -Eigenschaft in der Eigenschaften Tabelle auf eine Sprache festgelegt ist, die auch in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt ist.
5.  Wenn Sie ein Installationspaket für die erste Version Ihres Produkts erstellen, verwenden Sie einen neuen [**UpgradeCode**](upgradecode.md). Wenn das Paket für eine neuere Version eines vorhandenen Produkts vorgesehen ist oder die gleiche Version wie ein vorhandenes Produkt in einer anderen Sprache hat, verwenden Sie denselben [**UpgradeCode**](upgradecode.md) wie das vorhandene Produkt. Es können nicht zwei Produkte mit der gleichen [**ProductVersion**](productversion.md) und der gleichen [**productlanguage**](productlanguage.md) den gleichen [**UpgradeCode**](upgradecode.md)aufweisen, es sei denn, es handelt sich um ein [kleines Update](small-updates.md) der anderen Version.
6.  Der [**UpgradeCode**](upgradecode.md) hat das Format einer [GUID](guid.md). Geben Sie die [**UpgradeCode**](upgradecode.md) -GUID in die Eigenschaften Tabelle ein.

Weitere Informationen finden Sie unter [verhindern, dass ein altes Paket über eine neuere Version installiert](preventing-an-old-package-from-installing-over-a-newer-version.md)wird.

 

 



