---
title: Eigenschaften (IInertiaProcessor)
description: Dieser Abschnitt enthält die Eigenschaften für die IInertiaProcessor-Schnittstelle.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows-Berührungs-, IInertiaProcessor-Schnittstelle
- Windows-Fingereingabe, Schnittstelleneigenschaften
- Trägheit, IInertiaProcessor-Schnittstelle
- IInertiaProcessor-Schnittstelle, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab3e1754c7b723b4be446e82fd0ba39fc67af5d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391340"
---
# <a name="properties-iinertiaprocessor"></a>Eigenschaften (IInertiaProcessor)

Dieser Abschnitt enthält die Eigenschaften für die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle.



| Eigenschaft                                                                               | Beschreibung                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Gibt den horizontalen Ausgangs Speicherort für ein Ziel mit Intertia an.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Gibt den vertikalen Start Speicherort für ein Ziel mit Intertia an.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Gibt die anfängliche Bewegung des Zielobjekts auf der horizontalen Achse an.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Gibt die anfängliche Bewegung des Zielobjekts auf der vertikalen Achse an.                                |
| [**Initialangularvelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Gibt die Rotationsgeschwindigkeit des Ziels an, wenn die Bewegung beginnt.                                    |
| [**Initialexpansionvelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Gibt die Rate der RADIUS-Erweiterung des Ziels an, wenn die Bewegung beginnt.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Gibt den Abstand zwischen dem Rand des Ziels und seinem Mittelpunkt an, bevor das Objekt geändert wurde.          |
| [**Boundaryleft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Gibt an, wie weit das Zielobjekt in Richtung Links auf dem Bildschirm verschoben werden kann.                                 |
| [**Boundarytop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Begrenzt, wie weit das Zielobjekt verschoben werden kann.                                  |
| [**Boundaryright**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Schränkt an, wie weit die Rechte Seite des Bildschirms verschoben werden kann.                           |
| [**Boundarybottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Begrenzt, wie weit das Zielobjekt verschoben werden kann, bis zum unteren Bildschirmrand.                               |
| [**Elasticmarginleft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Gibt den linken linken Bereich für das Springen des Zielobjekts an.                                            |
| [**Elasticmargintop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Gibt den obersten Bereich für das Springen des Zielobjekts an.                                             |
| [**Elasticmarginright**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Gibt den äußersten rechten Bereich für das Springen des Zielobjekts an.                                           |
| [**Elasticmarginbottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Gibt die untere Region für das Springen des Zielobjekts an.                                              |
| [**Desiredangularverlangsamung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Gibt die gewünschte Rate an, mit der das Zielobjekt im Bogenmaße pro msec angehalten wird.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Gibt den gewünschten Abstand (im Bogenmaße) an, an dem ein Objekt vom Trägheits Prozessor bearbeitet wird. |
| [**Desiredexpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Gibt die gewünschte Änderung im durchschnittlichen Radius des-Objekts an.                                        |
| [**Desiredexpansionverlangsamung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Gibt die Rate an, mit der das Objekt nicht mehr erweitert wird.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Gibt die gewünschte Rate an, mit der Übersetzungs Vorgänge verlangsamt werden.                              |
| [**Eigenschaften desireddisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Gibt die gewünschte Entfernung an, die das Objekt übertragen wird.                                              |
| [**Initialtimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Gibt den Start Zeitstempel für ein Zielobjekt an, das Trägheit hat.                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




