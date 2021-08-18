---
title: Einstellungsparameter der Tastatur
description: Der Einstellungsparameter für die Tastatur gibt an, dass der Benutzer sich auf die Tastatur und nicht auf die Maus verlässt. Daher sollten Anwendungen Tastaturschnittstellen anzeigen, die andernfalls ausgeblendet würden.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c074078cdd548b6b3614213d6086edb3f5a6a412d84e418417dc0b4fcd2800e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998480"
---
# <a name="keyboard-preference-parameter"></a>Einstellungsparameter der Tastatur

Der Einstellungsparameter für die Tastatur gibt an, dass der Benutzer sich auf die Tastatur und nicht auf die Maus verlässt. Daher sollten Anwendungen Tastaturschnittstellen anzeigen, die andernfalls ausgeblendet würden.

Der Benutzer steuert die Einstellung des Einstellungsparameters für die Tastatur mithilfe des Center für erleicherte Bedienung in Systemsteuerung oder einer anderen Anwendung zum Anpassen der Umgebung. Anwendungen verwenden die **Flags SPI \_ GETKEYBOARDPREF** und **SPI \_ SETKEYBOARDPREF** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um den Einstellungsparameter der Tastatur abzurufen und festzulegen.

Darüber hinaus können Benutzer auf Windows 2000 einen Parameter festlegen, der angibt, ob Menüzugriffsschlüssel immer unterstrichen werden. Anwendungen verwenden die **FLAGS SPI \_ GETMENUUNDERLINES** und **SPI \_ SETMENUUNDERLINES** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um den Menüunterstreichungsparameter abzurufen und festzulegen.

Wenn eine Anwendung eine [**WM \_ SETTINGCHANGE-Nachricht**](/windows/desktop/winmsg/wm-settingchange) für den Tastaturpräferenz- oder Menü-Unterstreichungsparameter empfängt, wird empfohlen, dass die Anwendung [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) aufruft, um die Informationen für beide Parameter zu aktualisieren.

Beachten Sie, dass **SPI \_ GETMENUUNDERLINES** mit **SPI \_ GETKEYBOARDCUES** identisch ist und **SPI \_ SETMENUUNDERLINES** mit **SPI \_ SETKEYBOARDCUES** identisch ist.

 

 