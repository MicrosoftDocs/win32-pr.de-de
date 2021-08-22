---
description: ICE73 überprüft, ob Ihr Paket keine Paketcodes, Upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele wiederverwendet. Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts nie wiederverwenden.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e5beecbfc7b4345d3b0dd7a93b86c55acc1abde4cc4f99d72749368be9d303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635076"
---
# <a name="ice73"></a>ICE73

ICE73 überprüft, ob Ihr Paket keine Paketcodes, Upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele wiederverwendet. Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts nie wiederverwenden.

## <a name="result"></a>Ergebnis

ICE73 gibt eine Warnung aus, wenn das Paket Ihres Produkts ein Paket oder einen Produktcode eines Windows Installer SDK-Beispiels wiederverwendet.

## <a name="example"></a>Beispiel

ICE73 meldet die folgenden Fehler für das gezeigte Beispiel:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Die Sternchen ( ) in der GUID stellen den Bereich von GUIDs dar, die für nachfolgende Installer SDK Windows pakete \* \* \* \* reserviert sind.

 

Um die Fehler zu beheben, generieren Sie eine neue eindeutige GUID für die Produkt- und Paketcodes Ihres Pakets. Außerdem benötigen Sie eine neue eindeutige GUID für den Upgradecode Ihres Pakets.

[Zusammenfassungsinformationsstream](summary-information-stream.md) (partiell)



| Eigenschaft       | Wert                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-000000000047} |



 

[Eigenschaftentabelle](property-table.md) (partiell)



| Eigenschaft                           | Wert                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**Upgradecode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Paketcodes](package-codes.md)
</dt> <dt>

[Produktcodes](product-codes.md)
</dt> <dt>

[**Zusammenfassungseigenschaft für Revisionsnummer**](revision-number-summary.md)
</dt> <dt>

[**UpgradeCode-Eigenschaft**](upgradecode.md)
</dt> <dt>

[**ProductCode-Eigenschaft**](productcode.md)
</dt> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



