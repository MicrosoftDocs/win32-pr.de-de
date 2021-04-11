---
title: Referenz zum Windows-Ereignisprotokoll
description: Im folgenden finden Sie die Programmier Elemente, die Sie zum Erstellen eines Instrumentierungs Manifests, zum Erstellen von Ressourcen aus dem vom Anbieter verwendeten Manifest, zum erhalten von Instrumentations Metadaten zur Laufzeit und zum Abfragen von Ereignissen aus Kanälen und Protokolldateien verwenden.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041365"
---
# <a name="windows-event-log-reference"></a>Referenz zum Windows-Ereignisprotokoll

Im folgenden sind die Programmier Elemente aufgeführt, die Sie zum Erstellen eines Instrumentierungs Manifests, zum Erstellen von Ressourcen aus dem vom Anbieter verwendeten Manifest, zum erhalten von Instrumentations Metadaten zur Laufzeit und zum Abfragen von Ereignissen aus Kanälen und Protokolldateien verwenden:

-   [Event Manifest-Schema](eventmanifestschema-schema.md)
-   [Ereignis Schema](eventschema-schema.md)
-   [Abfrage Schema](queryschema-schema.md)
-   [Windows-Ereignisprotokoll Konstanten](windows-event-log-constants.md)
-   [Windows-Ereignisprotokoll Datentypen](windows-event-log-data-types.md)
-   [Windows-Ereignisprotokoll-Enumerationen](windows-event-log-enumerations.md)
-   [Windows-Ereignisprotokoll Funktionen](windows-event-log-functions.md)
-   [Windows-Ereignisprotokoll Strukturen](windows-event-log-structures.md)
-   [Windows-Ereignisprotokoll Tools](windows-event-log-tools.md)

Informationen zu Anwendungen, die mit einer .NET-Sprache geschrieben werden, z. b. c# oder Visual Basic, finden Sie in den folgenden Namespaces

-   Um Ereignisse zu schreiben, verwenden Sie die Klassen und Methoden, die im [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) -Namespace definiert sind.
-   Verwenden Sie die Klassen und Methoden, die im [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace definiert sind, um Ereignisse aus einem Windows-Ereignisprotokoll Kanal oder-Protokoll zu verarbeiten.

Als Alternative zur Verwendung des [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) -Namespace zum Schreiben von Ereignissen können Sie das **-CS-** oder **-CSS** -Argument verwenden, damit der Nachrichten Compiler den Code zum Schreiben der Ereignisse generiert. Weitere Informationen finden Sie unter [**Message Compiler**](message-compiler--mc-exe-.md).
