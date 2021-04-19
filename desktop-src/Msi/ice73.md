---
description: ICE73 überprüft, ob Paket Codes, upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele von Ihrem Paket nicht wieder verwendet werden. Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts niemals wieder verwenden.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347826"
---
# <a name="ice73"></a>ICE73

ICE73 überprüft, ob Paket Codes, upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele von Ihrem Paket nicht wieder verwendet werden. Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts niemals wieder verwenden.

## <a name="result"></a>Ergebnis

ICE73 gibt eine Warnung aus, wenn das Paket des Produkts ein Paket oder einen Produktcode eines Windows Installer SDK-Beispiels erneut verwendet.

## <a name="example"></a>Beispiel

ICE73 meldet die folgenden Fehler für das gezeigte Beispiel:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Die Sternchen ( \* \* \* \* ) in der GUID stellen den Bereich von GUIDs dar, der für nachfolgende Windows Installer SDK-Pakete reserviert ist.

 

Um die Fehler zu beheben, generieren Sie eine neue eindeutige GUID für das Produkt und die Paket Codes Ihres Pakets. Außerdem benötigen Sie eine neue eindeutige GUID für den UpgradeCode des Pakets.

[Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) (teilweise)



| Eigenschaft       | Wert                                  |
|----------------|----------------------------------------|
| PID- \_ revnumber | {000c1101-0000-0000-C000-000000000047} |



 

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft                           | Wert                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F 030-a751-11d2-A7D4-006097c99860} |
| [**UpgradeCode auch**](upgradecode.md) | {8fc70000-88a0-4b41-82b8-8905d4aa904c} |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Paket Codes](package-codes.md)
</dt> <dt>

[Produkt Codes](product-codes.md)
</dt> <dt>

[**Zusammenfassungs Eigenschaft der Revisionsnummer**](revision-number-summary.md)
</dt> <dt>

[**UpgradeCode-Eigenschaft**](upgradecode.md)
</dt> <dt>

[**ProductCode-Eigenschaft**](productcode.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



