---
title: Übergangs Schnittstellen
description: Dieser Abschnitt enthält die Referenz Spezifikationen für die Windows Animation Manager-Schnittstellen, die Übergänge unterstützen.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0110c44a1805c093f0872b62a4a21e13f29e00cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340834"
---
# <a name="transition-interfaces"></a>Übergangs Schnittstellen

Dieser Abschnitt enthält die Referenz Spezifikationen für die Windows Animation Manager-Schnittstellen, die Übergänge unterstützen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuianimationinterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Definiert Methoden zum Erstellen eines benutzerdefinierten interpolators.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Erweitert die [**iuianimationinterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) -Schnittstelle, die Methoden zum Erstellen eines benutzerdefinierten interpolators definiert. [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) unterstützt Interpolationen in einer bestimmten Dimension. <br/>        |
| [**Iuianimationprimitiveingeterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Definiert eine Methode, die einem benutzerdefinierten interpolators ermöglicht, Übergangsinformationen in Form einer kubischen polynomkurve an den Animations-Manager bereitzustellen.<br/>                                                                                                        |
| [**Iuianimationtransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Definiert einen Übergang, der bestimmt, wie sich eine Animations Variable im Laufe der Zeit ändert.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Erweitert die [**iuianimationtransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) -Schnittstelle, die einen Übergang definiert. Ein [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) -Übergang bestimmt, wie sich eine Animations Variable im Laufe der Zeit in einer bestimmten Dimension ändert.<br/> |
| [**Iuianimationtransitionfactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Definiert eine Methode zum Erstellen von Übergängen von benutzerdefinierten Interpolatoren.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Definiert eine Methode zum Erstellen von Übergängen von benutzerdefinierten Interpolatoren.<br/>                                                                                                                                                                                            |
| [**Iuianimationtransitionlibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Definiert eine Bibliothek von Standard Übergängen. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Definiert eine Bibliothek der Standard Übergänge für eine angegebene Dimension.<br/>                                                                                                                                                                                            |
| [**Iuianimationvariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Definiert eine Animations Variable, die ein visuelles Element darstellt, das animiert werden kann.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Definiert eine Animations Variable, die ein visuelles Element darstellt, das in mehreren Dimensionen animiert werden kann.<br/>                                                                                                                                                   |
| [**Iuianimationvariablechangehandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Definiert eine Methode für die Behandlung von Ereignissen, die sich auf Aktualisierungen von Animations Variablen beziehen.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Definiert eine Methode zur Behandlung von Aktualisierungs Ereignissen für Animations Variablen. [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) behandelt Ereignisse, die in einer angegebenen Dimension auftreten.<br/>                                                            |
| [**Iuianimationvariableintegerchangehandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Definiert eine Methode zur Behandlung von Aktualisierungs Ereignissen für Animations Variablen.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Definiert eine Methode zur Behandlung von Aktualisierungs Ereignissen für Animations Variablen. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) behandelt Ereignisse, die in einer angegebenen Dimension auftreten.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Definiert eine Methode zur Behandlung von Aktualisierungs Ereignissen für Animations Kurven. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](windows-animation-reference.md)
</dt> </dl>

 

 





