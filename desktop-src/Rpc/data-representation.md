---
title: Datendarstellung
description: Computingumgebungen können sich erheblich unterscheiden, ebenso wie Netzwerkarchitekturen.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Remoteprozeduraufruf RPC , beschrieben, Datendarstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9a0af96249c356f171396eaf52f91c5e33005eda080929cfbd8eecde27ffa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022090"
---
# <a name="data-representation"></a>Datendarstellung

Computingumgebungen können sich erheblich unterscheiden, ebenso wie Netzwerkarchitekturen. Um diesen Unterschieden gerecht zu werden, können Sie mit MIDL die Darstellung von Daten ändern. Manchmal können Sie die Entwicklung vereinfachen, indem Sie Daten in ein Format konvertieren, das Ihre Anwendung einfacher verarbeiten kann. Sie können das Datenformat Ihrer Anwendung ändern, damit sie effizienter über das Netzwerk übertragen werden kann.

Die Attribute transmit as und represent as weisen den Compiler an, einen **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** **\[** [**\_**](/windows/desktop/Midl/represent-as) transmissiblen Typ, den der Stub zwischen Client und Server übergibt, einem Benutzertyp zu zuordnen, den die Client- und **\]** Serveranwendungen verwenden. Sie müssen die Routinen, die die Konvertierung zwischen dem Benutzertyp und dem transmissiblen Typ durchführen, und die Routinen zur Freigabe des Arbeitsspeichers, der zum Halten der konvertierten Daten verwendet wurde, liefern. Die Verwendung **\[ des \_ Transmit-Attributs \]** als IDL-Attribut oder der **\[ -Darstellung \_ \]** als ACF-Attribut weist den Stub an, diese Konvertierungsroutinen vor und nach der Übertragung aufrufen. Mit **\[** [**dem Attribut "transmit \_ as"**](/windows/desktop/Midl/transmit-as) können Sie einen Datentyp für die Übertragung **\]** über das Netzwerk in einen anderen Datentyp konvertieren. Mit **\[** [**dem Attribut \_ "represent as"**](/windows/desktop/Midl/represent-as) können Sie steuern, wie Daten aus dem **\]** Netzwerk der Anwendung präsentiert werden.

Die **\[** [**Attribute wire \_ marshal**](/windows/desktop/Midl/wire-marshal) und user **\]** **\[** [**\_ marshal**](/windows/desktop/Midl/user-marshal) sind **\]** Microsoft-Erweiterungen der OSF-DCE-IDL. Ihre Syntax und Funktionalität ähneln der Der DCE-angegebenen **\[ \_ \]** Übertragung als und **\[ darstellen \_ \]** als Attribute bzw. Der Unterschied ist, dass Sie die Daten direkt marshallen, anstatt die Daten von einem Typ in einen anderen zu konvertieren. Hierzu müssen Sie die externen Routinen zum Anpassen der Größe des Datenpuffers auf client- und serverseitiger Seite, zum Marshallen und Zum Unmarshaling der Daten auf client- und serverseitiger Seite sowie zum Frei geben der Daten auf serverseitiger Seite verwenden. Der MIDL-Compiler generiert Formatcodes, die die NDR-Engine anweisen, diese externen Routinen bei Bedarf auf aufruft.

Die **\[ Attribute wire \_ marshal \]** und **\[ user \_ marshal \]** ermöglichen das Marshallen von Datentypen, die andernfalls nicht über Prozessgrenzen hinweg übertragen werden konnten. Da mit der Typkonvertierung weniger Aufwand verbunden ist, bieten **\[ wire \_ marshal \]** und **\[ user \_ marshal \]** zur Laufzeit eine verbesserte Leistung im **\[ \_ \]** Vergleich zur Übertragung als und **\[ darstellen \_ als \]**. Die **\[ Attribute "wire \_ marshal" \]** und **\[ "user \_ marshal" \]** **\[ \_ \]** **\[ \_ \]** schließen sich gegenseitig in Bezug aufeinander und in Bezug auf die Übertragung als und als Attribute für einen bestimmten Typ aus.

Beachten Sie, dass die Implementierung der Attribute **\[ wire \_ marshal \]** und **\[ user \_ marshal \]** den Marshallingregeln entsprechen muss, die von der OSF-DCE-Spezifikation festgelegt werden. Aus diesem Grund wird die Verwendung dieser Attribute nicht empfohlen, wenn Sie nicht mit dem Wire Protocol vertraut sind. Weitere Informationen zur NDR-Syntaxübertragung finden Sie unter [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Dieser Abschnitt bietet eine kurze Übersicht über diese für MIDL-Attribute in den folgenden Themen:

-   [**Die Übertragung \_ als und die Darstellung als \_ Attribute**](the-transmit-as-and-represent-as-attributes.md)
-   [**Wire \_ Marshal- und User \_ Marshal-Attribute**](the-wire-marshal-and-user-marshal-attributes.md)

 

 