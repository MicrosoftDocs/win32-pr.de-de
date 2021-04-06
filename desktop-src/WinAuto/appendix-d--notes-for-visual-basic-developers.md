---
title: Anhang D Hinweise für Visual Basic-Entwickler
description: Dieser Abschnitt enthält Informationen zu Microsoft-Active Accessibility für Entwickler von Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947660"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Anhang D: Hinweise für Visual Basic-Entwickler

Dieser Abschnitt enthält Informationen zu Microsoft-Active Accessibility für Entwickler von Microsoft Visual Basic.

In Visual Basic geschriebene Anwendungen sind Microsoft Active Accessibility-Clients. Sie stellen keine Informationen über Ihre benutzerdefinierten Benutzeroberflächen Elemente bereit, da Sie [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder keine andere Component Object Model (com)-Schnittstelle implementieren.

In dieser Dokumentation werden die C/C++-Namen für die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften verwendet; die Visual Basic Namen sind jedoch ähnlich. Beispielsweise würde die Eigenschaft [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) in einer Visual Basic Anwendung als **accName** bezeichnet.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Hinweise zur Visual Basic-Methode: accName](visual-basic-method-notes--accname.md)
-   [Hinweise zur Visual Basic-Methode: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Beispiel Programme](visual-basic-sample-programs.md)

 

 




