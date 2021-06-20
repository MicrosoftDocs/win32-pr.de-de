---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung mit Laufzeitkomponenten von APIs registrieren, die vom Windows Media Format 11 SDK bereitgestellt werden.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, Registrieren von Anwendungsabhängigkeiten
- Registrieren von Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406163"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)

Anwendungen, die APIs verwenden, die vom Windows Media Format SDK oder Windows Media Player SDK bereitgestellt werden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung im Rahmen der Anwendungseinrichtung als abhängig von diesen Komponenten registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig. Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine frühere Version blockiert. Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback. Stattdessen wird der Benutzer vor dem Ausführen des Rollbacks mit einer Meldung aufgefordert, dass Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der registrierungswert, der festgelegt werden soll, hängt von der Komponente ab, von der Ihre Anwendung abhängig ist. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung zur Verfügung zu stellen.

Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von der Windows Media Format SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Der folgende Registrierungswert wird verwendet, um die Abhängigkeit von Windows Media Player SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:

*REF \_ TYPE*

Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.

*APP*

Der Name oder kurze Deskriptor Ihrer Anwendung. Diese Zeichenfolge wird nicht in Meldungen verwendet, die für den Benutzer angezeigt werden. Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.

*\_APP-ZEICHENFOLGE*

Deskriptor Ihrer Anwendung. Diese Zeichenfolge kann in Meldungen verwendet werden, die für den Benutzer angezeigt werden.

*\_REF-DESKRIPTOR*

Beschreibung der Verwendung der Komponente durch Ihre Anwendung. Dieser Wert kann maximal 256 Zeichen enthalten.

*\_WMP-VERSION*

Version der Windows Media Player, die für Ihre Anwendung erforderlich ist.

*\_WMF-VERSION*

Version des Windows Media Format SDK, die für Ihre Anwendung erforderlich ist.

Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "South southplayer"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "South betriebssystemVideo", "South javascript Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überlegungen zum Projekt**](project-considerations.md)
</dt> </dl>

 

 




