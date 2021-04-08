---
title: Datendarstellung
description: Computerumgebungen können sich wie Netzwerkarchitekturen erheblich unterscheiden.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Datendarstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734537"
---
# <a name="data-representation"></a>Datendarstellung

Computerumgebungen können sich wie Netzwerkarchitekturen erheblich unterscheiden. Um diese Unterschiede zu unterstützen, können Sie mithilfe von "Mittel l" die Darstellung von Daten ändern. Manchmal können Sie die Entwicklung vereinfachen, indem Sie Daten in ein Format umrechnen, das von Ihrer Anwendung leichter verarbeitet werden kann. Sie können das Datenformat Ihrer Anwendung so ändern, dass es effizienter über das Netzwerk übertragen werden kann.

Die **\[** über [**Tragung \_ als**](/windows/desktop/Midl/transmit-as) **\]** und **\[** [**stellen \_ als Attribute dar**](/windows/desktop/Midl/represent-as) , **\]** die den Compiler anweisen, einen vom Stub zwischen Client und Server übermittelten Typ mit einem Benutzertyp zuzuordnen, der von den Client-und Server Anwendungen verwendet wird. Sie müssen die Routinen bereitstellen, mit denen die Konvertierung zwischen dem Benutzertyp und dem übertragbaren Typ durchgeführt wird, sowie die Routinen, um den Speicher freizugeben, der zum Speichern der konvertierten Daten verwendet wurde. Durch die Verwendung des Attributs "über **\[ tragen \_ als \]** IDL" oder des Attributs **\[ \_ als \]** ACF wird der Stub angewiesen, diese Konvertierungs Routinen vor und nach der Übertragung aufzurufen. **\[** Mit dem Attribut "über [**tragen \_ als**](/windows/desktop/Midl/transmit-as) " **\]** können Sie einen Datentyp für die Übertragung über das Netzwerk in einen anderen Datentyp konvertieren. Mithilfe des **\[** Attributs [**\_ As**](/windows/desktop/Midl/represent-as) **\]** können Sie steuern, wie Daten aus dem Netzwerk der Anwendung angezeigt werden.

Die **\[** Attribute " [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) " **\]** und " **\[** [**User \_ Marshal**](/windows/desktop/Midl/user-marshal) " **\]** sind Microsoft-Erweiterungen der OSF-DCE-IDL. Die Syntax und die Funktionen ähneln denen der von DCE angegebenen über **\[ Tragung \_ als \]** und **\[ repräsentieren \_ als \]** Attribute bzw. Der Unterschied besteht darin, dass Sie die Daten, anstatt die Daten von einem Typ in einen anderen zu wandeln, direkt Mars Hallen. Hierzu müssen Sie die externen Routinen zum Anpassen des Daten Puffers auf der Client-und Serverseite bereitstellen, die Daten auf der Client-und Serverseite Marshalling und das Marshalling von Daten durchführen und die Daten auf der Serverseite freigeben. Der mittlerer l-Compiler generiert Formatcodes, die die NDR-Engine anweisen, diese externen Routinen bei Bedarf aufzurufen.

Die Attribute " **\[ Wire \_ Marshal \]** " und " **\[ User \_ Marshal \]** " ermöglichen es, Datentypen zu Mars Hallen, die andernfalls nicht über Prozess Grenzen hinweg übertragen werden konnten. Da mit der Typkonvertierung weniger Aufwand verbunden ist, bieten der Übertragungs **\[ \_ Mars Hall \]** und der **\[ Benutzer- \_ Marshal \]** zur Laufzeit eine verbesserte Leistung, im Vergleich zu "über **\[ tragen \_ als \]** " und " **\[ darstellen \_ als \]**". Die Attribute " **\[ Wire \_ \] Marshal** " und " **\[ User \_ \] Marshal** " schließen sich gegenseitig und in Bezug auf die "über **\[ Tragung \_ als \]** **\[ \_ \] "-Attribute für** einen bestimmten Typ gegenseitig aus.

Beachten Sie unbedingt, dass die Implementierung der Attribute " **\[ Wire \_ Marshal \]** " und " **\[ User \_ Marshal \]** " den marshallingregeln entsprechen muss, die von der OSF-DCE-Spezifikation vorgegeben werden. Aus diesem Grund wird die Verwendung dieser Attribute nicht empfohlen, wenn Sie mit dem Wire-Protokoll nicht vertraut sind. Weitere Informationen zur Übertragung der NDR-Syntax finden Sie unter [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Dieser Abschnitt enthält eine kurze Übersicht über diese für Mittel l-Attribute in den folgenden Themen:

-   [**Die Übertragung \_ als und stellt \_ als Attribute dar.**](the-transmit-as-and-represent-as-attributes.md)
-   [**Die Attribute "Wire \_ Marshal" und "User \_ Marshal"**](the-wire-marshal-and-user-marshal-attributes.md)

 

 