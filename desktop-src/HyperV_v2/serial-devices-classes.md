---
description: Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen. Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Klassen für serielle Geräte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b95a2baaf4bc3dacfddf0e18f6acd88379f958e49fc1ccbd5d6ee5cf49a11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746107"
---
# <a name="serial-devices-classes"></a>Klassen für serielle Geräte

Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen. Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.

Die Einstellungen für den seriellen Controller sind nicht konfigurierbar. daher ist keine Einstellungsdateninstanz zugeordnet. Außerdem können Sie einem virtuellen Computer keine seriellen Controller oder seriellen Anschlüsse hinzufügen oder daraus entfernen. Daher gibt es keine Ressourcenpoolinstanzen für serielle Geräte.

Im Folgenden finden Sie Virtualisierungs-WMI-Klassen im Zusammenhang mit seriellen Geräten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | Beschreibung                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Stellt die Funktionen und die Verwaltung des seriellen Controllers dar.<br/> |
| [**Msvm \_ SerialPort**](msvm-serialport.md)<br/>                                     | Stellt einen seriellen Anschluss dar, der dem seriellen Controller zugeordnet ist.<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Ordnet einem seriellen Controller einen seriellen Anschluss zu.<br/>                   |



 

 

 




