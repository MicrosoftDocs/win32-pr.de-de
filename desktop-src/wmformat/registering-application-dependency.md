---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung bei Laufzeitkomponenten von APIs registrieren, die vom Windows Media Format 11 SDK bereitgestellt werden.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Medienformat-SDK, Registrieren von Anwendungsabhängigkeiten
- Registrieren von Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc0d1e6c9c5583ea235c196c244d9969aec65128dc206720cfacc907ae0067b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845905"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)

Anwendungen, die vom Windows Media Format SDK oder Windows Media Player SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung als abhängig von diesen Komponenten im Rahmen des Anwendungssetups registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig. Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine frühere Version blockiert. Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback. Stattdessen wird der Benutzer vor dem Rollback mit der Meldung aufgefordert, dass Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der festzulegende Registrierungswert hängt von der Komponente ab, von der Ihre Anwendung abhängig ist. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.

Die folgenden Registrierungswerte werden verwendet, um abhängigkeiten von der Windows Media Format SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Der folgende Registrierungswert wird verwendet, um abhängigkeiten von Windows Media Player SDK-Runtime zu registrieren:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:

*\_REF-TYP*

Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.

*APP*

Name oder Kurzbeschreibung Ihrer Anwendung. Diese Zeichenfolge wird nicht in Nachrichten verwendet, die für den Benutzer angezeigt werden. Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.

*\_APP-ZEICHENFOLGE*

Deskriptor Ihrer Anwendung. Diese Zeichenfolge kann in Nachrichten verwendet werden, die für den Benutzer angezeigt werden.

*\_REF-DESKRIPTOR*

Beschreibung, wie Ihre Anwendung die Komponente verwendet. Dieser Wert kann maximal 256 Zeichen enthalten.

*\_WMP-VERSION*

Die Version von Windows Media Player für Ihre Anwendung erforderlich.

*\_WMF-VERSION*

Version des für Ihre Anwendung erforderlichen Windows Media Format SDK.

Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ App, "South australiaVideo", "South australia Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "South australiaVideo", "Southselect Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Videodateien."
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "South australiaVideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Project Überlegungen**](project-considerations.md)
</dt> </dl>

 

 




