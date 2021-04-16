---
description: Parameterinformationen
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Parameterinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522187"
---
# <a name="parameter-information"></a>Parameterinformationen

Die [**imediaparaminfo:: getparaminfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) -Methode gibt eine [**MP- \_ paramInfo**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) -Struktur zurück, die einen Parameter beschreibt. Diese Struktur enthält die folgenden Informationen:

-   Der **mptype** -Member gibt den Datentyp des Parameter Werts an. Aus Effizienzgründen werden alle Parameter als 32-Bit-Gleit Komma Werte implementiert. Die [**MP- \_ Typenumeration**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) definiert, ob der Wert als ganze Zahl, Gleit Komma Wert, boolescher Wert oder Enumeration (ganzzahlige Reihen) interpretiert werden soll.
-   Der **mopcaps** -Member gibt an, welche Kurven dieser Parameter unterstützt. Wenn der Datentyp ein boolescher Wert oder eine Enumeration ist, ist die einzige Kurve, die der Parameter unterstützen kann, "springen".
-   Die Member **mpdminvalue** und **mpdmaxvalue** definieren die minimalen und maximalen Werte für diesen Parameter. Alle Kurven für diesen Parameter müssen in diesem Bereich liegen.
-   Der **mpdneutralvalue** -Member ist der Standardwert des-Parameters.
-   Der **szlabel** -Member ist der Name des Parameters, und der **szunittext** -Member ist der Name für die Maßeinheit für den Parameter. Beispiele hierfür sind "Volume" und "Decibels", "Frequency" und "kHz". Beide Zeichen folgen sind Englisch und werden nie lokalisiert. Der DMO kann lokalisierte Versionen über die [**imediaparaminfo:: getparamtext**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) -Methode bereitstellen.

Die Informationen zu den einzelnen Parametern bleiben während der gesamten Lebensdauer des DMO fest. Daher kann der Client diese Informationen einmal Abfragen und dann Zwischenspeichern.

**Zeitformate**

Der Client muss einen Zeitstempel für die Eingabedaten angeben, damit die entsprechenden Parameterwerte vom DMO berechnet werden können. Standardmäßig stellen Zeitstempel Einheiten von 100 Nanosekunden dar, die auch als *Bezugszeit* bezeichnet werden. Diese Zeiteinheit eignet sich jedoch nicht für jede Anwendung, sodass ein DMO über eine Option zur Unterstützung anderer Zeitformate verfügt. Zeitformate werden anhand der GUID identifiziert.



| **GUID**              | BESCHREIBUNG                   |
|-----------------------|-------------------------------|
| GUID- \_ Zeit \_ Verweis | Verweis Zeit                |
| Musik zur GUID- \_ Zeit \_     | Hinweis "Teile pro Quartal" (ppqn) |
| Beispiele für GUID- \_ Zeit \_   | Stichproben pro Sekunde            |



 

Drittanbietern wird empfohlen, bei Bedarf Ihre eigenen Zeitformate zu definieren. Allerdings müssen alle DMOS eine Verweis Zeit unterstützen. Dies stellt eine Standard Baseline dar, die von allen Benutzern verwendet werden kann. Um zu ermitteln, wie viele Zeitformate ein DMO unterstützt, müssen Sie die [**imediaparaminfo:: getnumtimeformats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) -Methode aufrufen. Um die unterstützten Formate aufzulisten, müssen Sie die [**imediaparaminfo:: getsupportedtimeformat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) -Methode aufrufen.

Um das Zeitformat festzulegen, müssen Sie [**imediaparams:: settimeformat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat)aufrufen. Diese Methode gibt die Zeitformat-GUID und die *Zeit Daten* an, d. h. die Anzahl der Einheiten pro Takt. Wenn beispielsweise das Zeitformat Samples pro Sekunde und die Uhrzeit Daten 32 sind, entspricht der Zeitstempelwert 10 320 Stichproben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Parameter](media-parameters.md)
</dt> </dl>

 

 



