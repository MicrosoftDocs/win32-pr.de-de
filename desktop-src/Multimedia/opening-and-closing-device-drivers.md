---
title: Öffnen und Schließen von Gerätetreibern
description: Öffnen und Schließen von Gerätetreibern
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Instrument Digital Interface (KEYBOARD), Öffnen von Geräten
- KEYBOARD (Keyboard Instrument Digital Interface), Öffnen von Geräten
- VERT-Dienste, Öffnen von Geräten
- Öffnen vonTE-Geräten
- Instrument Digital Interface (KEYBOARD), Schließen von Geräten
- KEYBOARD (Keyboard Instrument Digital Interface), Schließen von Geräten
- SCHLIEßEN VON DIENSTEN,Schließen von Geräten
- Schließen von SCHLIEßENDEN GERÄTEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e935ab3d0d420e735bed6e01d08c80962e134338ea9e88eaa4899e0e81cb71f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806290"
---
# <a name="opening-and-closing-device-drivers"></a>Öffnen und Schließen von Gerätetreibern

Bevor Sie es verwenden können, müssen Sie ein DANN-Gerät öffnen, und Sie sollten es schließen, sobald Sie es nicht mehr verwenden. Windows stellt die folgenden Funktionen zum Öffnen und Schließen verschiedener TYPEN-Gerätetypen zur Verfügung.



| Wert                                | Bedeutung                                            |
|--------------------------------------|----------------------------------------------------|
| [**keyboardInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Schließt ein angegebenes EINGABE-Eingabegerät.              |
| [**bei unsInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Öffnet ein angegebenes EINGABE-Eingabegerät für die Aufzeichnung. |
| [**dateiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Schließt ein angegebenes DANN-Ausgabegerät.             |
| [**ohne Sperre**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Öffnet ein DANN-Ausgabegerät für die Wiedergabe.           |



 

Jede Funktion, die ein BEZEICHNUNG-Gerät öffnet, verwendet als Parameter einen Gerätebezeichner, eine Adresse eines Speicherspeicherorts und einige Parameter, die für DIE-Geräte eindeutig sind. Der Speicherort wird mit einem Gerätehandpunkt gefüllt, der verwendet wird, um das geöffnete Audiogerät in Aufrufen anderer Audiofunktionen zu identifizieren.

VieleFUNKTIONsfunktionen können entweder ein Gerätehand handle oder einen Gerätebezeichner akzeptieren. Obwohl Sie ein Gerätehand handle überall dort verwenden können, wo Sie eine Geräte-ID verwenden würden, können Sie nicht immer einen Gerätebezeichner verwenden, wenn ein Handle aufgerufen wird.

> [!Note]  
> DIE Geräte sind nicht unbedingt sharable, sodass ein bestimmtes Gerät möglicherweise nicht verfügbar ist, wenn ein Benutzer es an fordert. In diesem Fall sollte die Anwendung den Benutzer benachrichtigen und dem Benutzer erlauben, das Gerät erneut zu öffnen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KEYBOARD-Dienste](midi-services.md)
</dt> </dl>

 

 