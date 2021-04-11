---
description: Die Sensor-API bietet eine Methode, die Sie verwenden können, um den Benutzer zur Eingabe von Berechtigungen für die Verwendung eines Sensors oder einer Sammlung von Sensoren aufzufordern.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Verwalten von Benutzerberechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958823"
---
# <a name="managing-user-permissions"></a>Verwalten von Benutzerberechtigungen

Die Sensor-API bietet eine Methode, die Sie verwenden können, um den Benutzer zur Eingabe von Berechtigungen für die Verwendung eines Sensors oder einer Sammlung von Sensoren aufzufordern.

Da Sensoren vertrauliche Informationen offenlegen können, erfordert Windows, dass Benutzer Sensoren aktivieren, bevor das Programm auf Daten zugreifen kann.

Möglicherweise möchten Sie die-Berechtigung anfordern, wenn Sie Sensoren verwenden möchten, für die der aktuelle [**sensorstate**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) -Sensor Zustands \_ \_ Zugriff \_ verweigert wurde.

Um Berechtigungen anzufordern, können Sie die Methode " [**isensormanager:: requestberechtigungs**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Methode" aufrufen. Wenn Sie diese Methode aufgerufen haben, öffnet Windows das Dialogfeld **Sensoren aktivieren** , in dem der Benutzer aufgefordert wird, die von Ihnen angeforderten Sensoren zu aktivieren. In diesem Dialogfeld werden dem Benutzer die Namen der von Ihnen angeforderten Sensoren bereitstellt. Der Benutzer kann eine der folgenden Optionen auswählen:

-   **Aktivieren Sie diese Sensoren**.
-   **Aktivieren Sie diese Sensoren nicht**.
-   **Öffnen Sie die Systemsteuerung, um weitere Optionen zu öffnen**.

Wenn ein Benutzer **diese Sensoren nicht aktivieren aktiviert**, zeigt Windows das Dialogfeld **Sensoren aktivieren** nicht erneut an, selbst wenn das Programm [**requestberechtigungs Berechtigungen**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)aufruft. Wenn der Benutzer eine andere Option auswählt, lässt Windows zu, dass das Dialogfeld angezeigt wird, wenn es angefordert wird. Wenn Ihr **requestberechtigungs** -Auflistungs paar Sensoren enthält, die der Benutzer zuvor für die Deaktivierung ausgewählt hat, entfernt die Sensor-API diese Sensoren aus der Liste der Sensoren, die dem Benutzer angezeigt werden.

### <a name="modal-or-modeless-behavior"></a>Modales oder nicht modales Verhalten

Die [**requestberechtigungs**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) -Methode nimmt ein **Boolesches** Argument an, das bestimmt, ob das Dialogfeld **Sensoren aktivieren** als modales oder nicht modales Fenster angezeigt wird. Diese Einstellung wirkt sich auch darauf aus, ob das Verhalten des Dialogfeld Rückgabecodes synchron oder asynchron ist.

Beim modalen wird der Fokus des Dialog Felds auf die Anwendungsfenster beschränkt, bis der Benutzer eine Option auswählt, und der **HRESULT** -Rückgabecode aus dem Aufrufen von [**requestberechtigungs**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Informationen gibt die Benutzer Auswahl an. Bei einem nicht modalem Fokus hat das Dialogfeld keinen exklusiven Fokus, und der **requestactivation** -Befehl wird sofort zurückgegeben. In diesem Fall gibt der Rückgabecode an, ob die Methode erfolgreich war, kann aber nicht verwendet werden, um die Auswahl des Benutzers zu ermitteln. Sie können dann ermitteln, welche Sensoren aktiviert wurden, indem Sie das [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) -Ereignis behandeln und die einzelnen Sensoren auf den Sensor \_ Status \_ vorbereiten.

Weitere Informationen zu Rückgabecodes finden Sie auf der Referenzseite zu [**requestberechtigungs Berechtigungen**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) .

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Bewährte Vorgehensweise: Vermeiden von mehreren nicht modalem Aufrufen von requestberechtigungs Berechtigungen

Bei wiederholten nicht modalem Aufrufen von [**requestberechtigungs Berechtigungen**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) werden mehrere Instanzen des Dialog Felds **diese Sensoren aktivieren** angezeigt, und der Bildschirm kann möglicherweise mit Dialogfeldern überflutet werden, was zu einem schlechten Benutzer Verhalten führt. Wenn Sie der Ansicht sind, dass nach dem ersten Aufrufen von **Request-Berechtigungen** andere Positionssensoren installiert werden können, die einen weiteren **requestberechtigungs** aufzurufen erfordern, sollten Sie entweder " **requestberechtigungen** " modale aufrufen oder warten, bis alle Speicherort Sensoren installiert sind, um einen nicht modalem Rückruf durchführen zu können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenschutz und Sicherheit auf der Plattform für Sensoren und Orte](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Anfordern von Benutzerberechtigungen](requesting-user-permissions.md)
</dt> </dl>

 

 
