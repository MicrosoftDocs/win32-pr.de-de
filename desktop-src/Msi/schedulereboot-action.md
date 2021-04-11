---
description: Fügen Sie die Aktion schedulereboot in die Aktions Sequenz ein, um den Benutzer zur Eingabe eines Neustarts des Systems am Ende der Installation aufzufordern. Verwenden Sie die ForceReboot-Aktion, um während der Installation zur Eingabe eines Neustarts aufzufordern.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Schedulereboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865196"
---
# <a name="schedulereboot-action"></a>Schedulereboot-Aktion

Fügen Sie die Aktion schedulereboot in die Aktions Sequenz ein, um den Benutzer zur Eingabe eines Neustarts des Systems am Ende der Installation aufzufordern. Verwenden Sie die [ForceReboot-Aktion](forcereboot-action.md) , um während der Installation zur Eingabe eines Neustarts aufzufordern.

Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm am Ende der Installation ein Meldungs Feld und eine Schaltfläche an, um zu Fragen, ob der Benutzer das System neu starten möchte. Der Benutzer muss auf diese Eingabeaufforderung Antworten, bevor die Installation abgeschlossen wird. Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System am Ende automatisch neu gestartet.

Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, wird der Benutzer automatisch aufgefordert, am Ende der Installation neu zu starten, unabhängig davon, ob in der Sequenz ForceReboot-oder schedulereboot-Aktionen vorhanden sind. Beispielsweise fordert das Installationsprogramm automatisch einen Neustart an, wenn es alle Dateien ersetzen muss, die während der Installation verwendet werden.

Sie können bestimmte Eingabe Aufforderungen für Neustarts unterdrücken, indem Sie die Eigenschaft [**Neustart**](reboot.md) festlegen.

Wenn die Windows Installer während einer [Installation mit mehreren Paketen](multiple-package-installations.md)auf die Aktion [ForceReboot](forcereboot-action.md) oder schedulereboot stößt, wird das Installationsprogramm beendet und führt ein Rollback der Installation aus. Andere Pakete, die zur Installation mit mehreren Paketen gehören und keine ForceReboot-oder schedulereboot-Aktion enthalten, können installiert werden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Diese Aktion kann z. b. verwendet werden, um das Installationsprogramm zu zwingen, nach der Installation von Treibern, die einen Neustart erfordern, nach einem Neustart zu Fragen. Wenn das Installationsprogramm versucht, Dateien zu ersetzen, die verwendet werden, wird der Benutzer automatisch zum Neustart aufgefordert, auch wenn schedulereboot nicht verwendet wurde.

Die schedulereboot-Aktion wird in der Regel am Ende der Sequenz abgelegt, aber Sie kann an einem beliebigen Punkt in der Sequenz eingefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Neustarts](system-reboots.md)
</dt> </dl>

 

 



