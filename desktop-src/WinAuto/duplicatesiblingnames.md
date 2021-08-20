---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115330"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Text

Doppelter gleichgeordneter Name+Rolle \\ " {0} \\ " verursacht Mehrdeutigkeit zwischen Elementen.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Ein Element hat denselben Namen und Role/ControlType wie ein anderes Element.

Dieses Problem kann zu Verwirrung führen, da Sprachausgabe den gleichen Text für alle Elemente mit demselben Namen und Role/ControlType liest.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Der Name des Elements enthält Role/ControlType-Text.
-   Der Name des Elements oder der Name des übergeordneten Elements ist nicht festgelegt oder falsch festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




