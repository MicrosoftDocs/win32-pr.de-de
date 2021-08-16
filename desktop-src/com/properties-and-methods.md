---
title: Eigenschaften und Methoden
description: Wie jedes OLE-Objekt stellt ein -Steuerelement einen Großteil seiner Funktionalität über eine Reihe eingehender Schnittstellen mit Eigenschaften und Methoden bereit.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dae30453089f235a4e70d7896569ebefcdff9f7f2419b5fc54af88b8563d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047888"
---
# <a name="properties-and-methods"></a>Eigenschaften und Methoden

Wie jedes OLE-Objekt stellt ein -Steuerelement einen Großteil seiner Funktionalität über eine Reihe eingehender Schnittstellen mit Eigenschaften und Methoden bereit.

Ein -Steuerelement macht Eigenschaften und Methoden durch OLE-Automatisierung verfügbar, sodass Container unter der Kontrolle einer vom Container bereitgestellten Programmiersprache darauf zugreifen können.

Um den Zugriff auf Eigenschaften über eine Benutzeroberfläche zu unterstützen, bietet ein -Steuerelement Eigenschaftenseiten, Unterstützung für OLEIVERB-EIGENSCHAFTEN, \_ durchsuchende Eigenschaften und Datenbindung über Eigenschaftsänderungs-Notficationen.

-   Über Eigenschaftenseiten kann ein Steuerelement seine Eigenschaften bei Bedarf unabhängig vom Container anzeigen.
-   Durch die Unterstützung von \_ OLEIVERB-EIGENSCHAFTEN wird das Element Eigenschaften im Menü des Containers angezeigt. Anschließend kann der Endbenutzer das **Element Eigenschaften** auswählen, um die Eigenschaftenseiten des Steuerelements anzuzeigen und die Eigenschaften zu ändern.
-   Das Durchsuchen pro Eigenschaft unterstützt einen Container, der die Eigenschaften des Steuerelements als Teil eines größeren Eigenschaftenblatts anzeigen kann, das Eigenschaften von mehreren Steuerelementen im Container enthalten kann.
-   Durch die Eigenschaftsänderungsbenachrichtigung kann ein Steuerelement einen Client benachrichtigen, dass sich seine Eigenschaften geändert haben, sodass der Client alle erforderlichen Aktionen ausführen kann.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Steuerelementeigenschaften](control-properties.md)
-   [Steuerelementmethoden](control-methods.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> <dt>

[Eigenschaftenseiten und Eigenschaftenblätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




