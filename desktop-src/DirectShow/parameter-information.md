---
description: Parameterinformationen
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Parameterinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe38cc9197df3ae22bcd72b824da5887647bca9e9d6101e3833d482fa907052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050770"
---
# <a name="parameter-information"></a>Parameterinformationen

Die [**IMediaParamInfo::GetParamInfo-Methode**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) gibt eine [**MP \_ PARAMINFO-Struktur**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) zurück, die einen Parameter beschreibt. Diese Struktur enthält die folgenden Informationen:

-   Der **mpType-Member** gibt den Datentyp des Parameterwerts an. Aus Effizienzgründen werden alle Parameter als 32-Bit-Gleitkommawerte implementiert. Die [**MP \_ TYPE-Enumeration**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) definiert, ob der Wert als ganze Zahl, Gleitkommawert, boolescher Wert oder Enumeration (ganzzahlige Reihe) interpretiert werden soll.
-   Das **mopCaps-Element** gibt an, welche Kurven dieser Parameter unterstützt. Wenn der Datentyp boolesch oder enumeration ist, ist die einzige Kurve, die der Parameter unterstützen kann, "Jump".
-   Die Member **mpdMinValue** und **mpdMaxValue** definieren die Minimal- und Höchstwerte für diesen Parameter. Alle Kurven für diesen Parameter müssen innerhalb dieses Bereichs liegen.
-   Der **mpdNeutralValue-Member** ist der Standardwert des Parameters.
-   Das **szLabel-Element** ist der Name des Parameters, und das **szUnitText-Element** ist der Name für die Maßeinheit für den Parameter. Beispiele hierfür sind "Volume" und "Decibels" oder "Frequency" und "kHz". Beide Zeichenfolgen sind Englisch und werden nie lokalisiert. Die DMO können lokalisierte Versionen über die [**IMediaParamInfo::GetParamText-Methode**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) bereitstellen.

Die Informationen für jeden Parameter bleiben während der gesamten Lebensdauer des DMO fest. Daher kann der Client diese Informationen einmal abfragen und dann zwischenspeichern.

**Zeitformate**

Der Client muss einen Zeitstempel der Eingabedaten verwenden, damit der DMO die entsprechenden Parameterwerte berechnen kann. Standardmäßig stellen Zeitstempel Einheiten von 100 Nanosekunden dar, die auch als *Referenzzeit* bezeichnet werden. Diese Zeiteinheit ist jedoch nicht für jede Anwendung geeignet, sodass ein DMO eine Option zur Unterstützung anderer Zeitformate hat. Zeitformate werden durch GUID identifiziert.



| **GUID**              | BESCHREIBUNG                   |
|-----------------------|-------------------------------|
| \_GUID-ZEITREFERENZ \_ | Referenzzeit                |
| GUID \_ TIME \_ MUSIC     | Hinweise zu Teilen pro Quartal (PPQN) |
| \_ \_ GUID-ZEITBEISPIELE   | Stichproben pro Sekunde            |



 

Dritten wird empfohlen, bei Bedarf eigene Zeitformate zu definieren. Allerdings müssen alle DMOs die Referenzzeit unterstützen. Dies stellt eine Standardbaseline bereit, die jeder verwenden kann. Um zu bestimmen, wie viele Zeitformate ein DMO unterstützt, rufen Sie die [**IMediaParamInfo::GetNumTimeFormats-Methode**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) auf. Um die unterstützten Formate aufzulisten, rufen Sie die [**IMediaParamInfo::GetSupportedTimeFormat-Methode**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) auf.

Rufen Sie [**IMediaParams::SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat)auf, um das Zeitformat festzulegen. Diese Methode gibt die GUID des Zeitformats und die *Zeitdaten* an. Dabei handelt es sich um die Anzahl der Einheiten pro Takt. Wenn das Zeitformat beispielsweise Stichproben pro Sekunde und die Zeitdaten 32 sind, entspricht ein Zeitstempelwert von 10 320 Stichproben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienparameter](media-parameters.md)
</dt> </dl>

 

 



