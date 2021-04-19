---
description: Der System Energiestatus gibt an, ob die Stromversorgung eines Computers eine System Batterie oder eine Stromversorgung ist. Bei Computern, die Akkus verwenden, gibt der System Energiestatus auch an, wie viel Akku Lebensdauer verbleiben und ob der Akku belastet wird.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: System Energie Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356160"
---
# <a name="system-power-status"></a>System Energie Status

Der System Energiestatus gibt an, ob die Stromversorgung eines Computers eine System Batterie oder eine Stromversorgung ist. Bei Computern, die Akkus verwenden, gibt der System Energiestatus auch an, wie viel Akku Lebensdauer verbleiben und ob der Akku belastet wird.

Energieinformationen werden abgerufen, indem Sie über die [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) -Funktion für Energie Einstellungs Benachrichtigungen registriert werden. Diese Funktion ermöglicht es Anwendungen, sich für bestimmte Energie Einstellungen zu registrieren und benachrichtigt zu werden, wenn Sie sich ändern.

> [!Note]  
> Verwenden Sie [**callntpowerinformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation), um Energiestatus Informationen ohne Benachrichtigungen abzufragen.

 

Anwendungen und installierbare Treiber verwenden normalerweise den System Energiestatus, um zu bestimmen, ob ein fortgesetzter Vorgang möglich ist. Bevor eine Anwendung z. b. Hintergrund Vorgänge durchführt, z. b. das komprimieren oder Paginieren einer Datei, sollte überprüft werden, ob es sich um ein System mit Batterien handelt. Ein weiteres Beispiel: eine Anwendung, die einen langwierigen Vorgang startet, sollte den Status überprüfen, um zu ermitteln, ob genügend Akkuleistung vorhanden ist, um den Vorgang abzuschließen.

Standardmäßig werden Anwendungen oder Treiber während des standbyübergangs vom System nicht abgefragt.

> [!Note]  
> Wenn die Stromversorgung gering ist, kann eine Anwendung einen Benutzereingriff anfordern oder anfordern, dass das System sich selbst anhält. Sie können den Systembetrieb mithilfe der [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) -Funktion aussetzen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> </dl>

 

 



