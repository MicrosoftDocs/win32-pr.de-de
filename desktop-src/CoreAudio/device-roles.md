---
description: Geräte Rollen
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Geräte Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126901"
---
# <a name="device-roles"></a>Geräte Rollen

Wenn ein System mindestens zwei audiorendering-Endpunkt Geräte enthält, kann ein Gerät am besten für die Wiedergabe eines audioinhaltstyp geeignet sein, und ein anderes Gerät eignet sich möglicherweise am besten für die Wiedergabe eines anderen Inhaltstyps. Wenn ein System z. b. über zwei renderinggeräte verfügt, kann der Benutzer auf einem Gerät Musik abspielen und System Benachrichtigungs Sounds auf dem anderen Gerät abspielen.

Wenn ein System mindestens zwei audioerfassungs-Endpunkt Geräte enthält, kann ein Gerät am besten zum Erfassen eines Audioinhalts Typs geeignet sein, und ein anderes Gerät eignet sich möglicherweise am besten zum Erfassen eines anderen Inhaltstyps. Wenn ein System beispielsweise über zwei Erfassungsgeräte verfügt, kann der Benutzer Live Musik auf einem Gerät aufzeichnen und das andere Gerät für Sprachbefehle verwenden.

Geräte können über drei Rollen verfügen: Console, Communications und Multimedia. in der folgenden Tabelle werden die Geräte Rollen beschrieben, die von den drei Konstanten – econsole, eCommunications und emultimedia – in der [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration identifiziert werden.



| Erole-Konstante  | Geräte Rolle                              | Renderingbeispiele             | Beispiele für die Erfassung                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| econsole        | Interaktion mit dem Computer            | Spiele und System Benachrichtigungen | Sprachbefehle                     |
| eCommunications | Sprachkommunikation mit einer anderen Person | Chat und VoIP                  | Chat und VoIP                      |
| emultimedia     | Abspielen oder Aufzeichnen von Audioinhalten       | Musik und Filme               | Erzählung und Live Musik Aufzeichnung |



 

Einem bestimmten Rendering-oder Aufzeichnungsgerät können keine, eine, einige oder alle Rollen in der vorangehenden Tabelle zugewiesen werden. Jede Rolle in der Tabelle wird immer einem (und nur einem) renderinggerät und einem (und nur einem) Erfassungsgerät zugewiesen. Das heißt, die Zuweisung von Rollen zum Rendern von Geräten ist unabhängig von der Zuweisung von Rollen zum Erfassen von Geräten.

Eine Anwendung kann Ihre gesamten Ausgabedaten Ströme über ein einzelnes renderingendpunkt-Gerät wiedergeben und alle Eingabedaten Ströme von einem einzelnen Erfassungs Endpunkt-Gerät aufzeichnen. Alternativ kann eine Anwendung ihre Ausgabedaten Ströme über ein renderinggerät wiedergeben und andere Ausgabedaten Ströme über ein anderes renderinggerät wiedergeben. Entsprechend kann es auch sein, dass einige der Eingabedaten Ströme über ein Erfassungsgerät aufgezeichnet werden und andere Eingabedaten Ströme über ein anderes Erfassungsgerät aufgezeichnet werden. In allen Fällen kann die Anwendung jeden Stream dem Gerät zuweisen, dessen Rolle für diesen Stream am besten geeignet ist.

Beispielsweise kann eine VoIP-Anwendung den Ausgabestream, der die Benachrichtigung über den Ring enthält, dem renderingendpunktgerät mit der econsole-Rolle zuweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[Arbeiten mit Geräte Rollen](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



