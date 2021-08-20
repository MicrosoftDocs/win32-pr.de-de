---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115357"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Text

Doppelte Automatisierungs-ID \\ " " führt zu {0} \\ Mehrdeutigkeit zwischen Elementen.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Ein Element verfügt über die gleiche Automation-ID wie ein anderes Element.

Dieses Problem kann Automatisierungsprobleme verursachen, die verhindern, dass Testcode auf das richtige Element verweist.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Gleichgeordnete Elemente verfügen über die gleiche Automation-ID.
-   Falsche Implementierung der UIA AutomationId-Eigenschaft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




