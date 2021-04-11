---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)
description: Anwendungs Abhängigkeit wird registriert
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media-Format-SDK, Registrieren von Anwendungsabhängigkeiten
- Anwendungsabhängigkeiten werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039914"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)

Anwendungen, die APIs verwenden, die vom Windows Media-Format-SDK oder Windows Media Player SDK bereitgestellt werden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung im Rahmen des Anwendungs Setups als von diesen Komponenten abhängig registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeits Ebenen auswählen: "blockieren" oder "abhängig". Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine vorherige Version blockiert. Abhängige Anwendungen, die nicht als Blockierung registriert sind, blockieren kein Rollback. Stattdessen wird der Benutzer vor dem Rollback aufgefordert, eine Meldung anzugeben, dass die Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der festzulegende Registrierungs Wert hängt von der Komponente ab, von der die Anwendung abhängt. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.

Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der SDK-Laufzeit des Windows Media-Formats zu registrieren:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Windows Media \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup Referenz \\ *\_ Typdeskriptor* \\ , "*App*", "*ref \_ Descriptor*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMF \_ Version*"

Der folgende Registrierungs Wert wird verwendet, um die Abhängigkeit von der Windows Media Player SDK-Laufzeit zu registrieren:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Descriptor, "*App*", "*ref \_ Descriptor*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMP \_ Version*"

In den oben aufgeführten Registrierungs Werten werden die folgenden Variablen verwendet:

*\_Verweistyp*

Ersetzen Sie dies durch blockingref Counts zum Blockieren der Abhängigkeit oder durch dependentref Counts für nicht blockierende Abhängigkeiten.

*APP*

Der Name oder der kurze Deskriptor Ihrer Anwendung. Diese Zeichenfolge wird nicht in Nachrichten verwendet, die für den Benutzer angezeigt werden. Dieser Wert ist der Bezeichner, der in allen drei Registrierungs Werten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.

*APP- \_ Zeichenfolge*

Deskriptor Ihrer Anwendung. Diese Zeichenfolge kann in Nachrichten verwendet werden, die für den Benutzer angezeigt werden.

*Verweis \_ Deskriptor*

Beschreibung der Verwendung der Komponente durch Ihre Anwendung. Dieser Wert kann maximal 256 Zeichen enthalten.

*WMP- \_ Version*

Die Version von Windows Media Player, die für Ihre Anwendung erforderlich ist.

*WMF- \_ Version*

Die Version des Windows Media-SDK, das für Ihre Anwendung erforderlich ist.

Die folgenden drei Beispiel Registrierungs Werte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ dependentrefcounts \\ app, "southridgevideo", "southridge Video Player"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ \\ Windows Media Setup \\ dependentrefcounts \\ Descriptor, "southridgevideo", "southridge Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Video Dateien".
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ dependentrefcounts \\ Version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überlegungen zu Projekten**](project-considerations.md)
</dt> </dl>

 

 




