---
title: Allgemeine Programmier Richtlinien
description: Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340506"
---
# <a name="general-programming-guidelines"></a>Allgemeine Programmier Richtlinien

In den folgenden Abschnitten werden allgemeine Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Anwendungs Kompatibilitäts Ebene](application-compatibility-layer.md)
</dt> <dd>

Zum Ausführen von Legacy Anwendungen in einer Remotedesktopdienste Umgebung können Sie die Remotedesktopdienste Anwendungs Kompatibilitäts Ebene verwenden.

</dd> <dt>

[Richtlinien für Client/Server-Anwendungen](client-server-application-guidelines.md)
</dt> <dd>

Client/Server-Anwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht.

</dd> <dt>

[Überwachen von Sitzungs Verbindungen und verbindungsverbindungen](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Um eine Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der virtuellen Kanal Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.

</dd> <dt>

[Richtlinien für Peripheriegeräte](peripheral-hardware-guidelines.md)
</dt> <dd>

Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.

</dd> <dt>

[Lauf Zeit Verknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

Die Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch mit der Wtsapi32.dll zu verknüpfen. Zu diesem Zweck sollte die Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zum Laden Wtsapi32.dll abrufen.

</dd> </dl>

 

 