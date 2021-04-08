---
description: ICE11 wird bei gleichzeitigen Installationen verwendet. Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter Parallele Installationen.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960041"
---
# <a name="ice11"></a>ICE11

ICE11 wird bei gleichzeitigen Installationen verwendet. Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).

## <a name="result"></a>Ergebnis

ICE11 überprüft die Quell Spalte der [CustomAction-Tabelle](customaction-table.md) mit benutzerdefinierten Aktionen für die gleichzeitige Installation. Die Quell Spalte muss eine gültige [GUID](guid.md) (MSI-Produktcode) enthalten.

ICE11 gibt einen Fehler aus, wenn die Quell Spalte der Tabelle CustomAction nicht ordnungsgemäß für benutzerdefinierte Aktionen der gleichzeitigen Installation erstellt wurde.

## <a name="example"></a>Beispiel

Ice gibt die folgenden Fehlermeldungen für das gezeigte Beispiel aus.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft        | Wert                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[CustomAction-Tabelle](customaction-table.md) (partiell)



| CustomAction | type | `Source`                                 |
|--------------|------|----------------------------------------|
| KA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| Ca2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Um die Fehler zu beheben, können Sie für CA1 keine gleichzeitige Installation des "Basispakets" durchführen. Dies führt zu einer rekursiven Installation. Dieser Eintrag sollte entfernt werden, oder die Quell Spalte sollte in eine GUID für eine angekündigte MSI geändert werden, die von der GUID des Basispakets abweicht. Legen Sie für Ca2 alle Zeichen der GUID in Großbuchstaben ab. Ändern Sie schließlich CA4's Source Column, um auf eine gültige GUID einer angekündigten MSI-Datei zu verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parallele Installationen](concurrent-installations.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



