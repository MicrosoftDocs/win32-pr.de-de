---
description: Die Sensor-API bietet eine Methode, mit der Sie den Benutzer zur Eingabe von Berechtigungen zur Verwendung eines Sensors oder einer Sammlung von Sensoren auffordern können.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Verwalten von Benutzerberechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02fac57959b493683d0fe0a007602e5a7af3f78dc959d0e7eca2811595c23dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576250"
---
# <a name="managing-user-permissions"></a>Verwalten von Benutzerberechtigungen

Die Sensor-API bietet eine Methode, mit der Sie den Benutzer zur Eingabe von Berechtigungen zur Verwendung eines Sensors oder einer Sammlung von Sensoren auffordern können.

Da Sensoren vertrauliche Informationen anzeigen können, erfordert Windows, dass Benutzer Sensoren aktivieren, bevor Ihr Programm auf Daten zugreifen kann.

Möglicherweise möchten Sie die Berechtigung anfordern, wenn Sie Sensoren verwenden möchten, für die der aktuelle [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) SENSOR \_ STATE ACCESS \_ \_ DENIED lautet.

Um Berechtigungen anzufordern, rufen Sie die [**ISensorManager::RequestPermissions-Methode auf.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Wenn Sie diese Methode aufrufen, öffnet Windows das Dialogfeld **Sensoren aktivieren,** um den Benutzer aufzufordern, die angeforderten Sensoren zu aktivieren. In diesem Dialogfeld werden dem Benutzer die Namen der angeforderten Sensoren angezeigt. Der Benutzer kann eine der folgenden Optionen auswählen:

-   **Aktivieren Sie diese Sensoren.**
-   **Aktivieren Sie diese Sensoren nicht.**
-   **Öffnen Sie Systemsteuerung für weitere Optionen.**

Wenn ein Benutzer **Diese Sensoren nicht aktivieren** ausgibt, zeigt Windows das Dialogfeld Sensoren **aktivieren** für diese bestimmten Sensoren nicht erneut an, auch wenn Ihr Programm [**RequestPermissions aufruft.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Wenn der Benutzer eine andere Option ausgibt, lässt Windows zu, dass das Dialogfeld auf Anforderung angezeigt wird. Wenn Ihr Aufruf von **RequestPermissions** einige Sensoren enthält, die der Benutzer zuvor ausgewählt hat, um deaktiviert zu bleiben, entfernt die Sensor-API diese Sensoren aus der Liste der Sensoren, die dem Benutzer angezeigt werden.

### <a name="modal-or-modeless-behavior"></a>Modales oder modusloses Verhalten

Die [**RequestPermissions-Methode**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) verwendet ein **boolesches** Argument, das bestimmt, ob das Dialogfeld **Sensoren aktivieren** als modales oder modusloses Fenster angezeigt wird. Diese Einstellung wirkt sich auch darauf aus, ob das Verhalten des Dialogfeldrückgabecodes synchron oder asynchron ist.

Bei modalem Modus hat das Dialogfeld den exklusiven Fokus zwischen Anwendungsfenstern, bis der Benutzer eine Option ausgibt und der **HRESULT-Rückgabecode** aus Ihrem Aufruf von [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) die Benutzerauswahl angibt. Wenn der Modus nicht aktiviert ist, hat das Dialogfeld keinen exklusiven Fokus, und Ihr Aufruf von **RequestPermissions** wird sofort zurückgegeben. In diesem Fall gibt der Rückgabecode an, ob die Methode erfolgreich war, aber nicht verwendet werden kann, um die Auswahl des Benutzers zu ermitteln. Sie können dann ermitteln, welche Sensoren aktiviert wurden, indem Sie das [**OnStateChanged-Ereignis**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) behandeln und jeden Sensor auf SENSOR \_ STATE READY \_ überprüfen.

Weitere Informationen zu Rückgabecodes finden Sie auf der [**Referenzseite RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Bewährte Methode: Vermeiden mehrerer modusloser Aufrufe von RequestPermissions

Wiederholte moduslose Aufrufe von [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) zeigen mehrere Instanzen des Dialogfelds **Diese Sensoren aktivieren** an und können den Bildschirm möglicherweise mit Dialogfeldern überfluten, was zu einer schlechten Benutzerfreundlichkeit führt. Wenn Sie der Meinung sind, dass nach dem ersten Aufruf von **RequestPermissions** möglicherweise andere Standortsensoren installiert sind, die einen weiteren Aufruf von **RequestPermissions** erfordern, sollten Sie entweder **RequestPermissions** modal aufrufen oder warten, bis alle Standortsensoren installiert sind, um einen moduslosen Aufruf zu tätigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenschutz und Sicherheit auf der Sensor- und Standortplattform](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Anfordern von Benutzerberechtigungen](requesting-user-permissions.md)
</dt> </dl>

 

 
