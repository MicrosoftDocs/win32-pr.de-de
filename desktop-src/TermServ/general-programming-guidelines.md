---
title: Allgemeine Programmierrichtlinien
description: Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b0e83daa98f59390408fa43f5c5f83ff547e3d0cad665d29922f4244913361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353881"
---
# <a name="general-programming-guidelines"></a>Allgemeine Programmierrichtlinien

Die folgenden Abschnitte enthalten allgemeine Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Anwendungskompatibilitätsschicht](application-compatibility-layer.md)
</dt> <dd>

Zum Ausführen von Legacyanwendungen in einer Remotedesktopdienste können Sie die Remotedesktopdienste Anwendungskompatibilitätsebene verwenden.

</dd> <dt>

[Client-/Serveranwendungsrichtlinien](client-server-application-guidelines.md)
</dt> <dd>

Client-/Serveranwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht.

</dd> <dt>

[Überwachen von Sitzungsverbindungen und -trennungen](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Um eine Anwendung bei Remotedesktopdienste registrieren, speichern Sie den Namen der Serveranwendung des virtuellen Kanals in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.

</dd> <dt>

[Richtlinien für Peripheriehardware](peripheral-hardware-guidelines.md)
</dt> <dd>

Wenn ihr Hardwaregerät nicht für die Verwendung über eine Remotesitzung konzipiert ist, müssen Anbieter sicherstellen, dass die Gerätetreibersoftware erzwingt, dass die Umleitung des Geräts mithilfe einer System- oder Gruppenrichtlinie deaktiviert wird.

</dd> <dt>

[Laufzeitverknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

Ihre Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch Wtsapi32.dll zu verknüpfen. Zu diesem Grund sollte Ihre Anwendung die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufrufen, um Wtsapi32.dll.

</dd> </dl>

 

 