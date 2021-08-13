---
title: Übergangsschnittstellen
description: Dieser Abschnitt enthält die Referenzspezifikationen für die Windows Animation Manager-Schnittstellen, die Übergänge unterstützen.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418600"
---
# <a name="transition-interfaces"></a>Übergangsschnittstellen

Dieser Abschnitt enthält die Referenzspezifikationen für die Windows Animation Manager-Schnittstellen, die Übergänge unterstützen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Definiert Methoden zum Erstellen eines benutzerdefinierten Interpolators.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Erweitert die [**IUIAnimationInterpolator-Schnittstelle,**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) die Methoden zum Erstellen eines benutzerdefinierten Interpolators definiert. [**IUIAnimationInterpolator2 unterstützt**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) die Interpolation in einer bestimmten Dimension. <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Definiert eine Methode, mit der ein benutzerdefinierter Interpolator Übergangsinformationen in Form einer kubischen polynomialen Kurve an den Animations-Manager bereitstellen kann.<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Definiert einen Übergang, der bestimmt, wie sich eine Animationsvariable im Laufe der Zeit ändert.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Erweitert die [**IUIAnimationTransition-Schnittstelle,**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) die einen Übergang definiert. Ein [**IUIAnimationTransition2-Übergang**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) bestimmt, wie sich eine Animationsvariable im Laufe der Zeit in einer bestimmten Dimension ändert.<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Definiert eine Methode zum Erstellen von Übergängen von benutzerdefinierten Interpolatoren.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Definiert eine Methode zum Erstellen von Übergängen von benutzerdefinierten Interpolatoren.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Definiert eine Bibliothek von Standardübergängen. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Definiert eine Bibliothek von Standardübergängen für eine angegebene Dimension.<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Definiert eine Animationsvariable, die ein visuelles Element darstellt, das animiert werden kann.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Definiert eine Animationsvariable, die ein visuelles Element darstellt, das in mehreren Dimensionen animiert werden kann.<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Definiert eine Methode zum Behandeln von Ereignissen im Zusammenhang mit Aktualisierungen von Animationsvariablen.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Definiert eine Methode zum Behandeln von Aktualisierungsereignissen für Animationsvariablen. [**IUIAnimationVariableChangeHandler2 behandelt**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) Ereignisse, die in einer angegebenen Dimension auftreten.<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Definiert eine Methode zum Behandeln von Aktualisierungsereignissen für Animationsvariablen.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Definiert eine Methode zum Behandeln von Aktualisierungsereignissen für Animationsvariablen. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) behandelt Ereignisse, die in einer angegebenen Dimension auftreten.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Definiert eine Methode zum Behandeln von Animationskurvenaktualisierungsereignissen. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](windows-animation-reference.md)
</dt> </dl>

 

 





