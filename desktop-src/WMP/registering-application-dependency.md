---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung bei Laufzeitkomponenten von APIs registrieren, die vom Windows Media Player SDK bereitgestellt werden.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,Anwendungsabhängigkeitsregistrierungseinstellungen
- Windows Media Player, Einstellungen für die Abhängigkeitsregistrierung
- Windows Media Player,Registrierung
- Registrierung, Anwendungsabhängigkeitseinstellungen
- Registrierung, Abhängigkeitseinstellungen
- Registrierung, Einstellungen für Windows Media Player
- Einstellungen für die Abhängigkeitsregistrierung
- Anwendungsabhängigkeitsregistrierungseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa210debc4045326eb3bbae1e4fc137db5fb5a5dec6b89e493aedd54f110f82f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861550"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)

Anwendungen, die vom Windows Media Player SDK oder Windows Media Format SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung als abhängig von diesen Komponenten im Rahmen des Anwendungssetups registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig. Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine frühere Version blockiert. Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback. Stattdessen wird dem Benutzer vor dem Rollback eine Meldung angezeigt, die besagt, dass Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der festzulegende Registrierungswert hängt von der Komponente ab, von der Ihre Anwendung abhängig ist. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.

Die folgenden Registrierungswerte werden verwendet, um abhängigkeiten von Windows Media Player SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Die folgenden Registrierungswerte werden verwendet, um abhängigkeiten von der Windows Media Format SDK Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:

*\_REF-TYP*

Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.

*APP*

Name oder Kurzbeschreibung Ihrer Anwendung. Diese Zeichenfolge wird nicht in Nachrichten verwendet, die für den Benutzer angezeigt werden. Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.

*\_APP-ZEICHENFOLGE*

Deskriptor Ihrer Anwendung. Diese Zeichenfolge kann in Nachrichten verwendet werden, die für den Benutzer angezeigt werden.

*\_REF-DESKRIPTOR*

Beschreibung der Verwendung der Komponente durch Ihre Anwendung. Dieser Wert kann maximal 256 Zeichen enthalten.

*\_WMP-VERSION*

Die Version von Windows Media Player für Ihre Anwendung erforderlich. Wenn keine Version angegeben wird, wird als Standardwert 9.0.0.0 angenommen.

*\_WMF-VERSION*

Version des Windows Media Format SDK, die für Ihre Anwendung erforderlich ist.

Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ App, "South australiaVideo", "South australia Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Descriptor, "South australiaVideo", "Southselect Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Videodateien."
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Version, "South australiaVideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




