---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung mit Laufzeitkomponenten von APIs registrieren, die vom Windows Media Player SDK bereitgestellt werden.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,Anwendungsabhängigkeitsregistrierungseinstellungen
- Windows Media Player,Einstellungen für die Abhängigkeitsregistrierung
- Windows Media Player,Registrierung
- Registrierung, Anwendungsabhängigkeitseinstellungen
- Registrierung, Abhängigkeitseinstellungen
- registry,settings for Windows Media Player
- Einstellungen für die Abhängigkeitsregistrierung
- Registrierungseinstellungen für Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407363"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)

Anwendungen, die vom Windows Media Player SDK oder Windows Media Format SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung im Rahmen der Anwendungseinrichtung als abhängig von diesen Komponenten registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig. Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert sind, wird die Komponente von einem Rollback auf eine frühere Version blockiert. Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback. Stattdessen wird dem Benutzer vor dem Rollback eine Meldung angezeigt, die besagt, dass Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der registrierungswert, der festgelegt werden soll, hängt von der Komponente ab, von der Ihre Anwendung abhängig ist. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung zur Verfügung zu stellen.

Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von Windows Media Player SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von der Windows Media Format SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:

*\_REF-TYP*

Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.

*APP*

Der Name oder kurze Deskriptor Ihrer Anwendung. Diese Zeichenfolge wird nicht in Meldungen verwendet, die für den Benutzer angezeigt werden. Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.

*\_APP-ZEICHENFOLGE*

Deskriptor Ihrer Anwendung. Diese Zeichenfolge kann in Meldungen verwendet werden, die für den Benutzer angezeigt werden.

*\_REF-DESKRIPTOR*

Beschreibung der Verwendung der Komponente durch Ihre Anwendung. Dieser Wert kann maximal 256 Zeichen enthalten.

*\_WMP-VERSION*

Version der Windows Media Player, die für Ihre Anwendung erforderlich ist. Wenn keine Version angegeben wird, wird als Standardwert 9.0.0.0 angenommen.

*\_WMF-VERSION*

Version des Windows Media Format SDK, die für Ihre Anwendung erforderlich ist.

Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "Southuda Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Descriptor, "South skriptvideo", "South javascript Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




