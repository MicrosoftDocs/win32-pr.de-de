---
title: Windows Ereignisprotokollreferenz
description: Im Folgenden finden Sie die Programmierelemente, mit denen Sie ein Instrumentierungsmanifest erstellen, Ressourcen aus dem Manifest erstellen, das Ihr Anbieter verwendet, Instrumentierungsmetadaten zur Laufzeit abrufen und Ereignisse aus Kanälen und Protokolldateien abfragen.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957790"
---
# <a name="windows-event-log-reference"></a>Windows Ereignisprotokollreferenz

Im Folgenden finden Sie die Programmierelemente, mit denen Sie ein Instrumentierungsmanifest erstellen, Ressourcen aus dem Manifest erstellen, das Ihr Anbieter verwendet, Instrumentierungsmetadaten zur Laufzeit abrufen und Ereignisse aus Kanälen und Protokolldateien abfragen:

-   [EventManifest-Schema](eventmanifestschema-schema.md)
-   [Ereignisschema](eventschema-schema.md)
-   [Abfrageschema](queryschema-schema.md)
-   [Windows Ereignisprotokollkonst constants](windows-event-log-constants.md)
-   [Windows Ereignisprotokolldatentypen](windows-event-log-data-types.md)
-   [Windows Ereignisprotokollenumeration](windows-event-log-enumerations.md)
-   [Windows Ereignisprotokollfunktionen](windows-event-log-functions.md)
-   [Windows Ereignisprotokollstrukturen](windows-event-log-structures.md)
-   [Windows Ereignisprotokolltools](windows-event-log-tools.md)

Informationen zu Anwendungen, die mit einer .NET-Sprache geschrieben wurden, z. B. C# oder Visual Basic, finden Sie in den folgenden Namespaces:

-   Verwenden Sie zum Schreiben von Ereignissen die Klassen und Methoden, die im [System.Diagnostics.Eventing-Namespace definiert](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) sind.
-   Um Ereignisse aus einem Windows Ereignisprotokollkanal oder -protokoll zu nutzen, verwenden Sie die Klassen und Methoden, die im [System.Diagnostics.Eventing.Reader-Namespace definiert](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) sind.

Als Alternative zur Verwendung des [System.Diagnostics.Eventing-Namespace](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) zum Schreiben von Ereignissen können Sie das **Argument -cs** oder **-css** verwenden, damit der Nachrichtencompiler den Code zum Schreiben der Ereignisse generiert. Weitere Informationen finden Sie unter [**Message Compiler**](message-compiler--mc-exe-.md).
