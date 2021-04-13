---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)
description: Anwendungs Abhängigkeit wird registriert
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, Registrierungs Einstellungen für Anwendungsabhängigkeiten
- Windows Media Player, Einstellungen für die Abhängigkeits Registrierung
- Windows Media Player, Registrierung
- Registrierung, Anwendungs Abhängigkeits Einstellungen
- Registrierung, Abhängigkeits Einstellungen
- Registrierung, Einstellungen für Windows-Media Player
- Abhängigkeits Registrierungs Einstellungen
- Registrierungs Einstellungen für Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474985"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)

Anwendungen, die vom Windows Media Player SDK oder Windows Media Format SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig. Sie können Ihre Anwendung im Rahmen des Anwendungs Setups als von diesen Komponenten abhängig registrieren.

Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeits Ebenen auswählen: "blockieren" oder "abhängig". Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert sind, wird die Komponente von einem Rollback auf eine vorherige Version blockiert. Abhängige Anwendungen, die nicht als Blockierung registriert sind, blockieren kein Rollback. Stattdessen wird dem Benutzer vor der Ausführung des Rollbacks eine Meldung angezeigt, die besagt, dass die Anwendungen von der Komponente abhängig sind.

Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert. Der festzulegende Registrierungs Wert hängt von der Komponente ab, von der die Anwendung abhängt. Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.

Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der Windows Media Player SDK-Laufzeit zu registrieren:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Descriptor, "*App*", "*ref \_ Descriptor*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMP \_ Version*"

Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der SDK-Laufzeit des Windows Media-Formats zu registrieren:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Windows Media \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup Referenz \\ *\_ Typdeskriptor* \\ , "*App*", "*ref \_ Descriptor*"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMF \_ Version*"

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

Die Version von Windows Media Player, die für Ihre Anwendung erforderlich ist. Wenn keine Version angegeben wird, wird angenommen, dass es sich bei dem Standardwert um 9.0.0.0 handelt.

*WMF- \_ Version*

Die Version des Windows Media-SDK, das für Ihre Anwendung erforderlich ist.

Die folgenden drei Beispiel Registrierungs Werte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:

-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ app, "southridgevideo", "southridge Video Player"
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ Descriptor, "southridgevideo", "southridge Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Video Dateien".
-   HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ Version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




