---
title: Joystick Funktionen
description: Joystick Funktionen
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- Multimedia-Eingabe, Joysticks
- Joysticks, zwei Achsenbewegung
- Joysticks, drei Achsenbewegung
- Joysticks, Schaltflächen
- Joysticks, bewegungsbereiche
- Joysticks, Abruf Häufigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726720"
---
# <a name="joystick-capabilities"></a>Joystick Funktionen

Joysticks können eine Bewegung mit zwei oder drei Achsen und bis zu vier Schaltflächen unterstützen. Außerdem unterstützen Joysticks verschiedene *Bereiche von Bewegungs* -und Abruf *Frequenzen*. Der Bewegungsbereich ist die Distanz, die ein Joystick Handle von seiner Ruheposition an die Position von der Ruheposition aus verschieben kann. Die Abruf Häufigkeit ist das Zeitintervall zwischen den Joystick Abfragen.

Joystick Treiber können entweder einen oder zwei Joysticks unterstützen. Sie können die Anzahl von Joystick ermitteln, die von einem Joystick Treiber unterstützt werden, indem Sie die Funktion " [**joygetnumdebug**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) " verwenden. Diese Funktion gibt eine ganze Zahl ohne Vorzeichen zurück, die die Anzahl unterstützter Joystick enthält, oder 0 (null), wenn keine Joystick Unterstützung vorhanden ist. Der Rückgabewert gibt nicht die Anzahl von Joystick an, die an das System angefügt sind.

Mithilfe der [**joygetpos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) -Funktion können Sie feststellen, ob ein Joystick mit dem System verbunden ist. Diese Funktion gibt "joyerr noError" zurück, \_ Wenn das angegebene Gerät angefügt wird. Andernfalls wird das joyerr-paar nicht getrennt zurückgegeben \_ .

Jeder Joystick verfügt über mehrere Funktionen, die für Ihre Anwendung verfügbar sind. Sie können die Funktionen eines Joystick mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion abrufen. Diese Funktion füllt eine [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) -Struktur mit Joystick Funktionen aus, z. b. die minimalen und maximalen Werte für das Koordinatensystem, die Anzahl der Schaltflächen auf dem Joystick und die minimalen und maximalen Abruf Frequenzen.

 

 