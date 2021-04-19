---
description: Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen. Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Serielle Geräteklassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360629"
---
# <a name="serial-devices-classes"></a>Serielle Geräteklassen

Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen. Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.

Die Einstellungen für den seriellen Controller sind nicht konfigurierbar. Daher ist keine Einstellungsdaten Instanz zugeordnet. Außerdem ist es nicht möglich, serielle Controller oder serielle Anschlüsse von einem virtuellen Computer hinzuzufügen oder zu entfernen. Daher sind keine Ressourcenpool Instanzen für serielle Geräte vorhanden.

Im folgenden finden Sie virtualisierungswmi-Klassen, die mit seriellen Geräten verknüpft sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | BESCHREIBUNG                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSVM \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Stellt die Funktionen und die Verwaltung des seriellen Controllers dar.<br/> |
| [**MSVM- \_ SerialPort**](msvm-serialport.md)<br/>                                     | Stellt einen seriellen Anschluss dar, der dem seriellen Controller zugeordnet ist.<br/>      |
| [**MSVM \_ serialportonserialcontroller**](msvm-serialportonserialcontroller.md)<br/> | Ordnet einen seriellen Anschluss einem seriellen Controller zu.<br/>                   |



 

 

 




