---
title: Uianameshouldnotcontaincontroltype
description: Uianameshouldnotcontaincontroltype
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855839"
---
# <a name="uianameshouldnotcontaincontroltype"></a>Uianameshouldnotcontaincontroltype

## <a name="text"></a>Text

Der Name des Elements ( {0} ) darf den Text des ControlType () nicht enthalten. {1}

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält seinen UIA-Steuer Elementtyp. Diese Warnung kann z. b. auftreten, wenn die UIA-Name-Eigenschaft für ein Element mit dem Steuer Elementtyp "Button" auf "My Button" festgelegt ist.

Dieses Problem führt dazu, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, den Steuerelement Typ zweimal lesen, oder dass er für Benutzer unerklärbar oder nicht intuitiv ist.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.
-   Das Element oder das übergeordnete Element verfügt über einen Standardnamen, der nicht auf einen anzeigen Amen überarbeitet wurde. Zum Beispiel: Button1.
-   Ein Entwickler weiß nicht, dass Bildschirm Sprachausgaben Namen und Steuerelement Typen lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




