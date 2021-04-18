---
title: DVC-Implementierungs Details
description: Dieser Abschnitt enthält Informationen zum Schreiben eines Client Moduls für einen dynamischen virtuellen Kanal (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341227"
---
# <a name="dvc-implementation-details"></a>DVC-Implementierungs Details

Dieser Abschnitt enthält Informationen zum Schreiben eines Client Moduls für einen dynamischen virtuellen Kanal (DVC).

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Schreiben eines Client-DVC-Moduls](writing-a-client-dvc-component.md)
</dt> <dd>

Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren.

</dd> <dt>

[DVC-Plug-in-Registrierung](dvc-plug-in-registration.md)
</dt> <dd>

Beschreibt die Syntax für den DVC (Dynamic Virtual Channel)-Plug-in-Eintrag für den Remotedesktopverbindung-Client (RDC).

</dd> <dt>

[Starten eines DVC-Listener](starting-a-dvc-listener.md)
</dt> <dd>

Zum Herstellen einer erfolgreichen Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel), die auf dem-Client und-Server des-Remotedesktopverbindung (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich in einem Empfangs Zustand befinden.

</dd> <dt>

[Akzeptieren einer Verbindung](accepting-a-connection.md)
</dt> <dd>

Zu einem bestimmten Zeitpunkt fordert der DVC-Client (Dynamic Virtual Channel) eine Verbindung mit dem DVC-Listener an.

</dd> <dt>

[Schreiben von Daten mithilfe eines DVC-Kanals](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch.

</dd> <dt>

[Testen und Debuggen](testing-and-debugging.md)
</dt> <dd>

Es gibt einen "Echo"-Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird, der immer vorhanden ist und auf eingehende Verbindungen lauscht.

</dd> <dt>

[Beispiel für DVC-Client-Plug-in](dvc-client-plug-in-example.md)
</dt> <dd>

C++-Codebeispiel, das veranschaulicht, wie Remotedesktopverbindung ein RDC-Client (Dynamic Virtual Channel)-Plug-in für Clients erstellt wird.

</dd> <dt>

[Beispiel für das DVC-Server Modul](dvc-server-component-example.md)
</dt> <dd>

C++-Codebeispiel, das zeigt, wie das serverseitige Dynamic Virtual Channel (DVC)-Modul erstellt wird.

</dd> </dl>

 

 




