---
title: Clientbereichs-Animationsparameter
description: Das Clientbereich-Animationsflag gibt an, ob der Benutzer Animationen in Benutzeroberflächenelementen deaktivieren möchte.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4d451424da0a02fa55efaead05ab285b3f07936167bb6e4376de4fd25ae11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325959"
---
# <a name="client-area-animation-parameter"></a>Clientbereichs-Animationsparameter

Der Animationsparameter des Clientbereichs gibt an, ob der Benutzer Animationen in Benutzeroberflächenelementen deaktivieren möchte. Anzeigefeatures wie Blinken, Blinken, Flackern und Verschieben von Inhalten können bei Benutzern mit fotoempfindlichen Blättern zu Löschungen führen. Mit diesem Parameter können Sie alle animationen dieser Art aktivieren oder deaktivieren.

Anwendungen verwenden die **Flags SPI \_ GETCLIENTAREAANIMATION** und **SPI \_ SETCLIENTAREAANIMATION** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um Clientbereichsanimationen zu aktivieren oder zu deaktivieren.

 

 