---
description: ICE11 wird mit gleichzeitigen Installationen verwendet. Gleichzeitige Installationen werden für die Installation von Anwendungen, die für die Veröffentlichung in der Öffentlichkeit vorgesehen sind, nicht empfohlen. Informationen zu gleichzeitigen Installationen finden Sie unter Gleichzeitige Installationen.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6e578cd6f7da09cc1894bc154ba77225f1efaafedf45f3fb7cdd3f30190e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119296490"
---
# <a name="ice11"></a>ICE11

ICE11 wird mit gleichzeitigen Installationen verwendet. Gleichzeitige Installationen werden für die Installation von Anwendungen, die für die Veröffentlichung in der Öffentlichkeit vorgesehen sind, nicht empfohlen. Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

## <a name="result"></a>Ergebnis

ICE11 überprüft die Spalte Quelle der [CustomAction-Tabelle](customaction-table.md) der gleichzeitigen benutzerdefinierten Installationsaktionen. Die Spalte Quelle muss eine gültige [GUID](guid.md) (MSI-Produktcode) enthalten.

ICE11 gibt einen Fehler aus, wenn die Spalte Quelle der CustomAction-Tabelle für benutzerdefinierte Aktionen zur gleichzeitigen Installation falsch erstellt wurde.

## <a name="example"></a>Beispiel

ICE sendet die folgenden Fehlermeldungen für das gezeigte Beispiel.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Eigenschaftentabelle](property-table.md) (partiell)



| Eigenschaft        | Wert                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[CustomAction-Tabelle](customaction-table.md) (partiell)



| CustomAction | Typ | Quelle                                 |
|--------------|------|----------------------------------------|
| KA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Um die Fehler zu beheben, können Sie für CA1 keine gleichzeitige Installation des "Basispakets" durchführen. Dies würde zu einer rekursiven Installation führen. Dieser Eintrag sollte entfernt oder die Spalte Quelle in eine GUID für eine angekündigte MSI geändert werden, die sich von der GUID des Basispakets unterscheidet. Erstellen Sie für CA2 alle Zeichen der GUID in Großbuchstaben. Ändern Sie abschließend die Spalte Quelle von CA4, um auf eine gültige GUID einer angekündigten MSI zu verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gleichzeitige Installationen](concurrent-installations.md)
</dt> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



