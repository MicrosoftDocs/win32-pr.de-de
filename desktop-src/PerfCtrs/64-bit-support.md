---
description: Wenn Sie Leistungsindikatoren auf einem 64-Bit-Computer bereitstellen, müssen Sie sowohl die 32-Bit-Version als auch die 64-Bit-Version des Anbieters auf dem Computer installieren, wenn Sie sowohl 32-Bit-als auch 64-Bit-Consumer unterstützen möchten.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: 64-Bit-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353463"
---
# <a name="64-bit-support"></a>64-Bit-Unterstützung

Eine 64-Bit-Leistungsdaten Anbieter-DLL kann nicht in einem 32-Bit-consumerprozess ausgeführt werden, und eine 32-Bit-Leistungsdaten Anbieter-DLL kann nicht in einem 64-Bit-Prozess ausgeführt werden. Die Anbieter Registrierung unterstützt nur einen einzelnen `Library` Wert für den Pfad zu ihrer Leistungsdaten Anbieter-DLL, sodass Sie keine unterschiedlichen Pfade bereitstellen können, die von 32-Bit-Consumern und 64-Bit-Consumern verwendet werden.

Die folgenden Optionen sind verfügbar, um v1-Anbieter auf 64-Bit-Betriebssystemen zu unterstützen:

- **Empfohlen:** Installieren Sie den Pfad für die 32-Bit-Version der Anbieter-DLL, und registrieren Sie ihn.
  - 32-Bit-Consumer arbeiten nativ: Sie laden die DLL des 32-Bit-Anbieters in den 32-Bit-consumerprozess.
  - 64-Bit-Consumer arbeiten indirekt: Sie können die DLL des 32-Bit-Anbieters nicht in den 64-Bit-consumerprozess laden. Windows greift jedoch automatisch auf einen 32-Bit-perfhost-Prozess zurück, lädt die dbit-Anbieter-DLL in den perfhost-Prozess und sendet Leistungsdaten vom 32-Bit-perfhost-Prozess an den 32-Bit-Consumer
- **nur 64-Bit:** Installieren Sie den Pfad für die 64-Bit-Version der Anbieter-DLL, und registrieren Sie ihn.
  - 32-Bit-Consumer können nicht ausgeführt werden: Sie können die DLL des 64-Bit-Anbieters nicht in den 32-Bit-Prozess laden.
  - 64-Bit-Consumer arbeiten nativ: Sie laden die DLL des 32-Bit-Anbieters in-Process.

> [!NOTE]
> Mehrere integrierte Windows-Leistungsdaten Anbieter installieren eine 32-Bit-DLL in `%systemroot%\syswow64` , installieren eine 64-Bit-DLL in `%systemroot%\system32` und registrieren den `Library` Pfad als `%systemroot%\system32\ProviderName.dll` , sodass die Dateisystem Umleitung den Pfad zur entsprechenden DLL auflösen kann. Dies wird nur für Leistungsdaten Anbieter unterstützt, die Teil des Windows-Betriebssystems sind. Anbieter, die nicht Teil des Windows-Betriebssystems sind, dürfen keine Dateien im `Windows` Ordner installieren. Nicht erkannte Dateien im `Windows` Ordner können während der Wartung oder des Upgrades entfernt werden.
