---
title: Eigenschaften und Methoden
description: Wie ein beliebiges OLE-Objekt stellt ein-Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereit.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036629"
---
# <a name="properties-and-methods"></a>Eigenschaften und Methoden

Wie ein beliebiges OLE-Objekt stellt ein-Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereit.

Ein-Steuerelement macht Eigenschaften und Methoden durch OLE-Automatisierung verfügbar, damit Container unter der Kontrolle über eine vom Container bereitgestellte Programmiersprache darauf zugreifen können.

Um den Zugriff auf Eigenschaften über eine Benutzeroberfläche zu unterstützen, stellt ein Steuerelement Eigenschaften Seiten, Unterstützung für oleiverb- \_ Eigenschaften, pro Durchsuchen von Eigenschaften und Datenbindung durch Eigenschafts Änderungen bereit.

-   Über Eigenschaften Seiten kann ein Steuerelement ggf. seine Eigenschaften unabhängig von seinem Container anzeigen.
-   Durch die Unterstützung von oleiverb \_ -Eigenschaften wird das Eigenschaften Element im Menü des Containers angezeigt. Anschließend kann der Endbenutzer das **Eigenschaften** Element auswählen, um die Eigenschaften Seiten des Steuer Elements anzuzeigen und die Eigenschaften zu ändern.
-   Pro Eigenschaften-Browsen unterstützt einen Container, der die Eigenschaften des Steuer Elements als Teil eines größeren Eigenschaften Blatts anzeigen kann, das Eigenschaften aus mehreren Steuerelementen im Container enthalten kann.
-   Mithilfe der Benachrichtigung über Eigenschafts Änderungen kann ein Steuerelement einen Client Benachrichtigen, dass seine Eigenschaften geändert wurden, sodass der Client alle notwendigen Aktionen ausführen kann.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Steuerelement Eigenschaften](control-properties.md)
-   [Steuerungsmethoden](control-methods.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> <dt>

[Eigenschaften Seiten und Eigenschaften Blätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




