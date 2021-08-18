---
description: Wenn Sie Leistungsindikatoren auf einem 64-Bit-Computer bereitstellen, müssen Sie sowohl die 32-Bit- als auch die 64-Bit-Version Ihres Anbieters auf dem Computer installieren, wenn Sie sowohl 32-Bit- als auch 64-Bit-Consumer unterstützen möchten.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: 64-Bit-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9756a6eaf95097c881368bc3f150422f494dac04e503da5060f27355827a653c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011428"
---
# <a name="64-bit-support"></a>64-Bit-Unterstützung

Eine 64-Bit-Leistungsdatenanbieter-DLL kann nicht in einem 32-Bit-Consumerprozess ausgeführt werden, und eine 32-Bit-Leistungsdatenanbieter-DLL kann nicht in einem 64-Bit-Prozess ausgeführt werden. Die Anbieterregistrierung unterstützt nur einen einzelnen `Library` Wert für den Pfad zu Ihrer Leistungsdatenanbieter-DLL, sodass Sie keine anderen Pfade bereitstellen können, die von 32-Bit-Consumern und 64-Bit-Consumern verwendet werden sollen.

Die folgenden Optionen sind verfügbar, um V1-Anbieter unter 64-Bit-Betriebssystemen zu unterstützen:

- **Empfohlen:** Installieren und registrieren Sie den Pfad zur 32-Bit-Version Ihrer Anbieter-DLL.
  - 32-Bit-Consumer funktionieren nativ: Sie laden Ihre 32-Bit-Anbieter-DLL in den 32-Bit-Consumerprozess.
  - 64-Bit-Consumer funktionieren indirekt: Sie können Ihre 32-Bit-Anbieter-DLL nicht in den 64-Bit-Consumerprozess laden, aber Windows greifen automatisch auf das Erstellen eines 32-Bit-Perfhost-Prozesses zurück, laden Ihre 32-Bit-Anbieter-DLL in den perfhost-Prozess und senden Leistungsdaten vom 32-Bit-Perfhost-Prozess an den 64-Bit-Consumerprozess.
- **Nur 64-Bit:** Installieren und registrieren Sie den Pfad zur 64-Bit-Version Ihrer Anbieter-DLL.
  - 32-Bit-Consumer schlagen fehl: Sie können Ihre 64-Bit-Anbieter-DLL nicht in den 32-Bit-Prozess laden.
  - 64-Bit-Consumer funktionieren nativ: Sie laden ihre 32-Bit-Anbieter-DLL in-Process.

> [!NOTE]
> Mehrere integrierte Windows Leistungsdatenanbieter installieren eine 32-Bit-DLL in `%systemroot%\syswow64` , installieren eine 64-Bit-DLL in und registrieren den Pfad als , sodass die `%systemroot%\system32` `Library` `%systemroot%\system32\ProviderName.dll` Dateisystemumleitung den Pfad zur entsprechenden DLL auflösen kann. Dies wird nur für Leistungsdatenanbieter unterstützt, die Teil des Windows Betriebssystems sind. Anbieter, die nicht Teil des Windows Betriebssystems sind, dürfen keine Dateien im `Windows` Ordner installieren. Nicht erkannte Dateien im `Windows` Ordner können während der Wartung oder des Upgrades entfernt werden.
