---
title: Uianamelengthtoolong
description: Uianamelengthtoolong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- AutomationElement. NameProperty des UIA_NamePropertyId Bezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388652"
---
# <a name="uianamelengthtoolong"></a>Uianamelengthtoolong

## <a name="text"></a>Text

Der Element Name darf keine Zeichenfolge zurückgeben, die länger als Zeichen ist. {0}

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält zu viele Zeichen. Beispielsweise gibt die [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) -Methode, die verwendet wird, um den UIA-Namen eines Elements abzurufen, eine Zeichenfolge zurück, die den Grenzwert überschreitet.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.

## <a name="possible-causes"></a>Mögliche Ursachen

Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




