---
title: Dupligonesiblingnames
description: Dupligonesiblingnames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714513"
---
# <a name="duplicatesiblingnames"></a>Dupligonesiblingnames

## <a name="text"></a>Text

Doppelter neben geordneter Name + Rolle \\ "" führt zu {0} \\ Mehrdeutigkeit zwischen Elementen.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element hat denselben Namen und dieselbe Rolle bzw. diesen Typ wie ein anderes Element.

Dieses Problem kann Verwirrung verursachen, da Sprachausgaben denselben Text für alle Elemente mit dem gleichen Namen und der gleichen Rolle bzw. dem gleichen "ControlType" lesen.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Der Name des Elements enthält den Text Role/ControlType.
-   Der Name des Elements oder der Name des übergeordneten Elements ist nicht festgelegt oder falsch festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> <dt>

[**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Iuiautomationelement. currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




