---
title: Tastatur Einstellungsparameter
description: Der Parameter "Keyboard Preference" gibt an, dass der Benutzer die Tastatur anstelle der Maus verlässt. Daher sollten Anwendungen Tastatur Schnittstellen anzeigen, die andernfalls ausgeblendet werden.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390563"
---
# <a name="keyboard-preference-parameter"></a>Tastatur Einstellungsparameter

Der Parameter "Keyboard Preference" gibt an, dass der Benutzer die Tastatur anstelle der Maus verlässt. Daher sollten Anwendungen Tastatur Schnittstellen anzeigen, die andernfalls ausgeblendet werden.

Der Benutzer steuert die Einstellung des Parameters "Keyboard Preference" mithilfe der Easy of Access Center in der Systemsteuerung oder einer anderen Anwendung für die Anpassung der Umgebung. Anwendungen verwenden die **SPI \_ getkeyboardpref** -und **SPI \_ setkeyboardpref** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Parameter für die Tastatur Präferenz zu erhalten und festzulegen.

Außerdem können Benutzer unter Windows 2000 einen Parameter festlegen, der angibt, ob Menü Zugriffstasten immer unterstrichen werden. Anwendungen verwenden die **SPI \_ getmenustrichen** -und **SPI \_ setmenustreicht** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Parameter "Menu-Unterstriche" zu erhalten und festzulegen.

Wenn eine Anwendung eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht für den Parameter Tastatur Preference oder Menu-Unterstreichung empfängt, wird empfohlen, dass die Anwendung [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) aufruft, um die Informationen für beide Parameter zu aktualisieren.

Beachten Sie, dass **SPI \_ getmenustreicht** mit **SPI \_ getkeyboardcues** identisch ist, und **SPI \_ setmenustreicht** mit **SPI \_ setkeyboardcues** identisch ist.

 

 