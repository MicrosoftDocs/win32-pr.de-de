---
title: Funktionen von "Capabilities"
description: Funktionen von "Capabilities"
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- Multimediaeingabe, -en
- Drehungen, Zwei-Achsen-Bewegung
- Drehungen, Drei-Achsen-Bewegung
- Schalter, Schaltflächen
- Drehungen, Bewegungsbereiche
- Frequenzen,Abrufhäufigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311109468485a8174d9567516e747ef786019cc105c378ee91b55fa2f123c5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140448"
---
# <a name="joystick-capabilities"></a>Funktionen von "Capabilities"

Die Zwei- oder Drei-Achsen-Bewegung und bis zu vier Schaltflächen können unterstützt werden. Außerdem unterstützen Diesser verschiedene *Bereiche von Bewegung* und *Abrufhäufigkeiten.* Der Bewegungsbereich ist der Abstand, den ein Ziehpunkt von seiner Ruheposition zu der Position bewegen kann, die von seiner Ruheposition am weitesten entfernt ist. Die Abrufhäufigkeit ist das Zeitintervall zwischen Abfrageabfragen.

Autotreiber können entweder ein oder zwei Gänge unterstützen. Sie können die Anzahl der von einem Fahrer unterstützten Autos ermitteln, indem Sie die [**funktiongetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) verwenden. Diese Funktion gibt eine ganze Zahl ohne Vorzeichen zurück, die die Anzahl der unterstützten 800er-Zeichen enthält, oder 0 (null), wenn keine Unterstützung vorhanden ist. Der Rückgabewert gibt nicht die Anzahl der Anfügezeichen an, die an das System angefügt sind.

Sie können mithilfe der Funktion [**"getPos"**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) ermitteln, ob ein Kasten an das System angefügt ist. Diese Funktion gibt DEN NOERROR-Fehler VOM 1. Tag \_ zurück, wenn das angegebene Gerät angeschlossen ist. Andernfalls wird DIE \_ UNPLUGGED-ENTPLUGGED-Datei zurückgegeben.

Jeder Manding verfügt über mehrere Funktionen, die für Ihre Anwendung verfügbar sind. Sie können die Funktionen eines Würfes abrufen, indem Sie die [**funktiongetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) verwenden. Diese Funktion füllt eine [**BUTTONCAPS-Struktur**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) mit Funktionen wie den minimalen und maximalen Werten für das Koordinatensystem, der Anzahl der Schaltflächen auf dem Kasten und der minimalen und maximalen Abrufhäufigkeit.

 

 