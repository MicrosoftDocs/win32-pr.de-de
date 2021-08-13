---
title: Plug-In-Referenz
description: Adapterfunktionen, Wrapperfunktionen und Strukturen zum Erstellen benutzerdefinierter Plug-In-Adapter mit drei Typen, Engine, Sensor und Speicher.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- Windows Biometrieframework-API Windows Biometrieframework-API, Plug-In-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2223f398579663d94c0cc40daef1fcf37e4239d8d0dc8246fedd15b454b3354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410960"
---
# <a name="plug-in-reference"></a>Plug-In-Referenz

Biometrische Geräte werden in einer Vielzahl von Typen und Konfigurationen hergestellt. Das Windows Biometric Framework umfasst eine erweiterbare Architektur, mit der Sie diese Vielfalt umgehen können, indem Sie benutzerdefinierte Plug-Ins erstellen. Im Mittelpunkt dieser Architektur steht ein Softwareobjekt, das als biometrische Einheit bezeichnet wird. Sie können sich eine biometrische Einheit als Abstraktion überlegen, die ein biometrisches Gerät für das Framework darstellt. Plug-In-Softwarekomponenten, die als Adapter bezeichnet werden, verbinden die biometrische Einheit mit der zugehörigen Hardware. Es gibt drei Arten von Adaptern, die Sie erstellen können. Ein Engine-Adapter generiert biometrische Vorlagen aus erfassten Beispielen, stimmt Beispiele mit vorhandenen Vorlagen ab und indiziert Vorlagen. Ein Sensoradapter umschließt ein biometrisches Gerät und stellt eine Standardschnittstelle zum Konfigurieren des Sensors, Erfassen von Stichproben und Steuern des Flusses biometrischer Daten an das Verarbeitungsmodul bereit. Ein Speicheradapter verwaltet Vorlagendatenbanken.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Plug-In-Funktionen](plug-in-functions.md)<br/>                 | Funktionen, die Sie verwenden können, um die Adapter-Plug-Ins zu erstellen, aus denen eine biometrische Einheit erstellt wird.<br/>                                                                     |
| [Plug-In-Strukturen](plug-in-structures.md)<br/>               | Strukturen für die Clientanwendungsentwicklung durch die Windows Biometrieframework-API.<br/>                                                                   |
| [Plug-In-Wrapperfunktionen](plug-in-wrapper-functions.md)<br/> | Wrapperfunktionen, mit denen Sie eine öffentliche Funktion auf einem beliebigen Adapter aufrufen können, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu erhalten.<br/> |



 

 

 





