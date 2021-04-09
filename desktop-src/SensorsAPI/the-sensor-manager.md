---
description: Das Sensor-Manager-Objekt ermöglicht den Zugriff auf die Sensoren, die für ihre Verwendung verfügbar sind.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Das Sensor-Manager-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128740"
---
# <a name="the-sensor-manager-object"></a>Das Sensor-Manager-Objekt

Das Sensor-Manager-Objekt ermöglicht den Zugriff auf die Sensoren, die für ihre Verwendung verfügbar sind.

Um die Sensor-API zu verwenden, müssen Sie zuerst die com- **cokreateinstance** -Methode aufrufen, um eine Instanz des Sensor-Manager-Objekts zu erstellen und einen Zeiger auf die Schnittstelle mit dem Namen " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)" abzurufen. Der Sensor-Manager verwaltet die Liste der verfügbaren Sensoren. Sie können " **isensormanager** " zum Aufrufen von Methoden verwenden, die Gruppen von Sensoren nach Kategorie oder nach Typ abrufen, oder Sie können eine Methode aufrufen, um einen bestimmten Sensor mithilfe der eindeutigen ID abzurufen. Der Sensor-Manager ermöglicht Ihnen außerdem die Registrierung, um ein Ereignis zu erhalten, mit dem Sie benachrichtigt werden, wenn ein neuer Sensor mit der Plattform verbunden ist.

Manchmal stellt der Sensor-Manager einen Zeiger auf einen Sensor bereit, der Benutzer hat den Sensor jedoch nicht aktiviert. Beispielsweise können Sie häufig Werte für nicht private Sensoreigenschaften abrufen, z. b. den Sensorhersteller oder das Modell, bevor der Benutzer den Sensor aktiviert. Anhand dieser Informationen können Sie entscheiden, ob der Benutzer zur Verwendung des Sensors aufgefordert werden soll. Sie können " [**isensormanager:: requestberechtigungs Berechtigungen**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) " aufrufen, um den Benutzer aufzufordern, einen bestimmten Sensor oder eine Sammlung von Sensoren zu aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Benutzerberechtigungen](managing-user-permissions.md)
</dt> <dt>

[Anfordern von Benutzerberechtigungen](requesting-user-permissions.md)
</dt> </dl>

 

 
