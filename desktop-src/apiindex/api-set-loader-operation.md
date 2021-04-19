---
description: Beschreibt, wie Windows 10 API-Sätze in Lade Ladevorgängen verwendet.
title: API-Satz-Ladevorgang
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106367258"
---
# <a name="api-set-loader-operation"></a>API-Satz-Ladevorgang

[API-Sätze](windows-apisets.md) basieren auf der Betriebssystemunterstützung im Bibliotheks Lade Modul, um eine Modul Namespace Umleitung in den Bibliotheks Bindungsprozess einzuführen. Der [Name des API-Satz Vertrags](windows-apisets.md#api-set-contract-names) wird vom Bibliotheks Lade Programm verwendet, um eine Lauf Zeit Umleitung des Verweises auf eine Ziel Host Binärdatei auszuführen, die die entsprechende Implementierung des API-Satzes enthält.

Wenn das Lade Programm zur Laufzeit auf eine Abhängigkeit von einem API-Satz stößt, konsultiert das Lade Programm Konfigurationsdaten im Abbild, um die Host Binärdatei für einen API-Satz zu identifizieren. Diese Konfigurationsdaten werden als **API-Set-Schema** bezeichnet. Das Schema wird als Eigenschaft des Betriebssystems assembliert, und die Zuordnung zwischen API-Sätzen und Binärdateien kann sich je nachdem, welche Binärdateien in einem bestimmten Gerät enthalten sind, unterscheiden. Das Schema ermöglicht, dass eine importierte Funktion in einer einzelnen Binärdatei auf verschiedenen Geräten ordnungsgemäß weitergeleitet wird, auch wenn die Modulnamen des binären Hosts auf verschiedenen Windows-Geräten umbenannt oder vollständig umgestaltet wurden.

Windows 10 unterstützt zwei Standardverfahren für die Nutzung und die Verwendung von API-Sets: **direkt Weiterleitung** und **Rück Weiterleitung**.

### <a name="direct-forwarding"></a>Direkte Weiterleitung

In dieser Konfiguration importiert der Konsumierende Code einen API-Satz Modulnamen direkt. Dieser Import wird in einem einzigen Vorgang aufgelöst und ist die effizienteste Methode mit dem geringsten Aufwand. Konzeptionell kann diese Lösung auf verschiedene Binärdateien auf verschiedenen Windows 10-Geräten verweisen, wie im folgenden Beispiel gezeigt:

Importierter API-Satz: **api-feature1-l1-1-0.dll**
-  Windows-PC-> **feature1.dll**
-  Hololens-> **feature1_holo.dll**
-  IOT-> **feature1_iot.dll**

Da die Zuordnungen in einem benutzerdefinierten Schema-Datenrepository aufbewahrt werden, bedeutet dies, dass ein API-Satz Name, der mit " **. dll** " endet, nicht direkt auf eine Datei auf dem Datenträger verweist. Der **dll** -Teil des API-Satz namens ist nur eine Konvention, die vom Lade Modul benötigt wird. Der Name des API-Satzes ähnelt eher einem Alias oder einem virtuellen Namen für eine physische dll-Datei. Dadurch ist der Name über den gesamten Bereich von Windows 10-Geräten portabel.

### <a name="reverse-forwarding"></a>Umgekehrte Weiterleitung

Während API-Satz Namen einen stabilen Namespace für Geräte übergreifende Module bereitstellen, ist es nicht immer praktikabel, jede Binärdatei in dieses neue System zu konvertieren. Beispielsweise kann eine Anwendung seit vielen Jahren häufig verwendet werden, und das erneute Kompilieren der Binärdateien der Anwendung ist möglicherweise nicht möglich. Außerdem müssen einige Anwendungen möglicherweise weiterhin auf Systemen ausgeführt werden, die vor der Einführung bestimmter API-Sets erstellt wurden.

Um diesem Kompatibilitäts Grad Rechnung zu tragen, werden auf allen Windows 10-Geräten, die eine Teilmenge der Win32-API-Oberfläche abdecken, ein *weiterforwardsystem* bereitgestellt. Diese Weiterleitungen verwenden die Modulnamen, die auf Windows-PCs eingeführt wurden, und nutzen das API-Set-System, um die Kompatibilität über alle Windows 10-Geräte hinweg zu gewährleisten.

Der Ladevorgang verhält sich wie folgt:

1.  Auf einem anderen Gerät als einem Windows-PC wird dem Lade Modul eine ältere Windows-PC-Modul namens Abhängigkeit präsentiert, die auf dem Gerät nicht vorhanden ist.
2.  Das Lade Modul sucht eine API-Satz Weiterleitung für dieses Modul und lädt Sie in den Arbeitsspeicher.
3.  Die Weiterleitung weist eine Zuordnung für den API-Satz für die angegebene Funktion auf, die aufgerufen wird.
4.  Das Lade Programm findet die richtige Host Binärdatei für das angegebene Gerät.

Konzeptionell sieht die Zuordnung wie folgt aus:

Importierte dll: **feature1.dll**
- Windows-PC-> **feature1.dll**
- Hololens-> **feature1.dll** Weiterleitung-> **api-feature1-l1-1-0.dll**  ->  **#d2**
- IOT-> **feature1.dll** Weiterleitung-> **api-feature1-l1-1-0.dll**  ->  **#d2**

Das Endergebnis ist funktional identisch mit der [direkten Weiterleitung](#direct-forwarding), wird jedoch auf eine Weise erreicht, die die Anwendungs Kompatibilität maximiert.

> [!NOTE]
> Die umgekehrte Weiterleitung bietet nur eine Teilmenge der Win32-API-Oberfläche. Anwendungen, die auf Desktop Versionen von Windows 10 ausgerichtet sind, können nicht auf allen Windows 10-Geräten ausgeführt werden.
