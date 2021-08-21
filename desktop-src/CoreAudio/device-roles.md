---
description: Geräterollen
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Geräterollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386a3ba163a9a82d01aa7916139edaa01e531160f5245c6e751fb7169702de5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018433"
---
# <a name="device-roles"></a>Geräterollen

Wenn ein System zwei oder mehr Audiorendering-Endpunktgeräte enthält, ist ein Gerät möglicherweise am besten für die Wiedergabe eines Audioinhaltstyps und ein anderes Gerät am besten für die Wiedergabe anderer Inhaltstypen. Wenn ein System z. B. über zwei Renderinggeräte verfügt, kann der Benutzer auswählen, ob er Musik auf einem Gerät und Systembenachrichtigungs-Sounds auf dem anderen wiedersingen soll.

Wenn ein System zwei oder mehr Audioaufnahmeendpunktgeräte enthält, ist ein Gerät möglicherweise am besten für die Erfassung eines Audioinhaltstyps, und ein anderes Gerät ist möglicherweise am besten für die Erfassung anderer Inhaltstypen. Wenn ein System beispielsweise über zwei Aufzeichnungsgeräte verfügt, kann der Benutzer live Musik auf einem Gerät aufzeichnen und das andere Gerät für Sprachbefehle verwenden.

Geräte können drei Rollen haben: Konsole, Kommunikation und Multimedia. In der folgenden Tabelle werden die Geräterollen beschrieben, die durch die drei Konstanten (eConsole, eCommunications und eMultimedia) in der [**ERole-Enumeration**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) identifiziert werden.



| ERole-Konstante  | Geräterolle                              | Renderingbeispiele             | Erfassungsbeispiele                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interaktion mit dem Computer            | Spiele und Systembenachrichtigungen | Sprachbefehle                     |
| eCommunications | Sprachkommunikation mit einer anderen Person | Chat und VoIP                  | Chat und VoIP                      |
| eMultimedia     | Wieder abspielen oder Aufzeichnen von Audioinhalten       | Musik und Filme               | Sprachausgabe und Live-Musikaufzeichnung |



 

Einem bestimmten Rendering- oder Erfassungsgerät können keine, eine, einige oder alle Rollen in der obigen Tabelle zugewiesen werden. Jede Rolle in der Tabelle wird jederzeit einem (und nur einem) Renderinggerät und einem (und nur einem) Erfassungsgerät zugewiesen. Das heißt, die Zuweisung von Rollen zu Renderinggeräten ist unabhängig von der Zuweisung von Rollen zum Erfassen von Geräten.

Eine Anwendung kann alle Ausgabestreams über ein einzelnes Renderingendpunktgerät wieder geben und alle Eingabestreams von einem einzigen Aufzeichnungsendpunktgerät aufzeichnen. Alternativ kann eine Anwendung auswählen, dass einige ihrer Ausgabestreams über ein Renderinggerät und andere Ausgabestreams über ein anderes Renderinggerät wieder verwendet werden. Auf ähnliche Weise kann es einige seiner Eingabestreams über ein Erfassungsgerät aufzeichnen und andere Eingabestreams über ein anderes Erfassungsgerät aufzeichnen. In allen Fällen kann die Anwendung jeden Stream dem Gerät zuweisen, dessen Rolle für diesen Stream am besten geeignet ist.

Beispielsweise kann eine VoIP-Anwendung dem Renderingendpunktgerät mit der eConsole-Rolle den Ausgabestream zuweisen, der die Ringbenachrichtigung enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[Arbeiten mit Geräterollen](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilität mit Legacyaudio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



