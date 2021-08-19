---
title: Eigenschaften (IInertiaProcessor)
description: Dieser Abschnitt enthält die Eigenschaften für die IInertiaProcessor-Schnittstelle.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Touch,IInertiaProcessor-Schnittstelle
- Windows Touch,Schnittstelleneigenschaften
- inertia,IInertiaProcessor-Schnittstelle
- IInertiaProcessor-Schnittstelle,Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7825a97545c897f402144ce5113b79650b9eba31e19da7ceef1459ae6cdc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030124"
---
# <a name="properties-iinertiaprocessor"></a>Eigenschaften (IInertiaProcessor)

Dieser Abschnitt enthält die Eigenschaften für die [**IInertiaProcessor-Schnittstelle.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)



| Eigenschaft                                                                               | Beschreibung                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Gibt die horizontale Startposition für ein Ziel mit Trägheit an.                                   |
| [**InitialOriginy**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Gibt die vertikale Anfangsposition für ein Ziel mit Trägheit an.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Gibt die anfängliche Bewegung des Zielobjekts auf der horizontalen Achse an.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Gibt die anfängliche Bewegung des Zielobjekts auf der vertikalen Achse an.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Gibt die Drehgeschwindigkeit des Ziels an, wenn die Bewegung beginnt.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Gibt die Radiuserweiterungsrate des Ziels an, wenn die Bewegung beginnt.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Gibt den Abstand zwischen dem Rand des Ziels und seinem Mittelpunkt an, bevor das -Objekt geändert wurde.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Schränkt ein, wie weit das Zielobjekt nach links vom Bildschirm bewegt werden kann.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Schränkt ein, wie weit das Zielobjekt nach oben auf dem Bildschirm bewegt werden kann.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Schränkt ein, wie weit das Zielobjekt auf der rechten Seite des Bildschirms bewegt werden kann.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Schränkt ein, bis zum unteren Bildschirmrand das Zielobjekt bewegt werden kann.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Gibt den äußersten linken Bereich zum Springen des Zielobjekts an.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Gibt den obersten Bereich für das Springen des Zielobjekts an.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Gibt den äußersten rechten Bereich zum Springen des Zielobjekts an.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Gibt den unteren Bereich für das Springen des Zielobjekts an.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Gibt die gewünschte Rate an, mit der das Zielobjekt die Drehung im Bogenmaß pro Msec stoppt.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Gibt den gewünschten Abstand (im Bogenmaß) an, in dem ein Objekt vom Trägheitsprozessor bearbeitet wird. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Gibt die gewünschte Änderung im durchschnittlichen Radius des Objekts an.                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Gibt die Rate an, mit der das Objekt nicht mehr erweitert wird.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Gibt die gewünschte Rate an, mit der Übersetzungsvorgänge verlangsamt werden.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Gibt den gewünschten Abstand an, den das Objekt zurückgibt.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Gibt den Startzeitstempel für ein Zielobjekt mit Trägheit an.                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iinertiaprocessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




