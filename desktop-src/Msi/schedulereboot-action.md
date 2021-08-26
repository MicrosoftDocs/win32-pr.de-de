---
description: Fügen Sie die Aktion ScheduleReboot in die Aktionssequenz ein, um den Benutzer am Ende der Installation zur Eingabe eines Neustarts des Systems aufforderungen. Verwenden Sie die ForceReboot-Aktion, um während der Installation zur Eingabe eines Neustarts aufforderungen.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: ScheduleReboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e796338c04f47ff4b2907dcf8d1531d438622a2f28a653e8ac4672a8b445e1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041520"
---
# <a name="schedulereboot-action"></a>ScheduleReboot-Aktion

Fügen Sie die Aktion ScheduleReboot in die Aktionssequenz ein, um den Benutzer am Ende der Installation zur Eingabe eines Neustarts des Systems aufforderungen. Verwenden Sie die [ForceReboot-Aktion,](forcereboot-action.md) um während der Installation zur Eingabe eines Neustarts aufforderungen.

Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm ein Meldungsfeld und eine Schaltfläche am Ende der Installation an und fragt, ob der Benutzer das System neu starten möchte. Der Benutzer muss auf diese Aufforderung reagieren, bevor er die Installation abgeschlossen hat. Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System am Ende automatisch neu gestartet.

Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, fordert es den Benutzer automatisch auf, am Ende der Installation neu zu starten, unabhängig davon, ob in der Sequenz ForceReboot- oder ScheduleReboot-Aktionen ausgeführt werden. Beispielsweise fordert das Installationsprogramm automatisch zur Eingabe eines Neustarts auf, wenn dateien ersetzt werden müssen, die während der Installation verwendet werden.

Sie können bestimmte Aufforderungen für Neustarts unterdrücken, indem Sie die [**REBOOT-Eigenschaft**](reboot.md) festlegen.

Wenn der Windows Installer während einer Installation mit mehreren Paketen die Aktion [ForceReboot](forcereboot-action.md) oder ScheduleReboot [findet,](multiple-package-installations.md)wird die Installation vom Installationsprogramm beenden und ein Rollback für die Installation ausgeführt. Andere Pakete, die zur Installation mehrerer Pakete gehören und keine ForceReboot- oder ScheduleReboot-Aktion enthalten, können installiert werden.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Diese Aktion kann beispielsweise verwendet werden, um zu erzwingen, dass das Installationsprogramm nach der Installation von Treibern, die einen Neustart erfordern, zur Eingabe eines Neustarts aufgefordert wird. Wenn das Installationsprogramm versucht, verwendete Dateien zu ersetzen, fordert es den Benutzer automatisch zum Neustart auf, auch wenn ScheduleReboot nicht verwendet wurde.

Die ScheduleReboot-Aktion wird in der Regel am Ende der Sequenz platziert, kann jedoch jederzeit in der Sequenz eingefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemneustarts](system-reboots.md)
</dt> </dl>

 

 



