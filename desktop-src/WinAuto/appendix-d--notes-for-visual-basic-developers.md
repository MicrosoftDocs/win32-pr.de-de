---
title: Anhang D – Hinweise für Visual Basic-Entwickler
description: Dieser Abschnitt enthält Informationen zu Microsoft Active Accessibility für Microsoft Visual Basic-Entwickler.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a857aeb8e04a0648d991e26913f9a9cf5c35328c62ed3f1ac3903a267e5a4e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122420"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Anhang D: Hinweise für Visual Basic-Entwickler

Dieser Abschnitt enthält Informationen zu Microsoft Active Accessibility für Microsoft Visual Basic-Entwickler.

In Visual Basic geschriebene Anwendungen sind Microsoft Active Accessibility Clients. Sie stellen keine Informationen zu ihren benutzerdefinierten Benutzeroberflächenelementen bereit, da sie [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder eine andere com-Schnittstelle (Component Object Model) nicht implementieren.

In dieser Dokumentation werden die C/C++-Namen für die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verwendet. die Visual Basic-Namen sind jedoch ähnlich. Beispielsweise würde die [**IAccessible::get \_ accName-Eigenschaft**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) in einer Visual Basic Anwendung **als accName** bezeichnet werden.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Visual Basic Hinweise zur Methode: accName](visual-basic-method-notes--accname.md)
-   [Visual Basic Hinweise zur Methode: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Beispielprogramme](visual-basic-sample-programs.md)

 

 




