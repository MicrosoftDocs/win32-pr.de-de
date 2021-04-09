---
title: Geräte Abfragen im Mixer
description: Geräte Abfragen im Mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- Multimedia-Audiodaten, Mixer-Geräte Abfragen
- Audiodaten, Mixer-Geräte Abfragen
- Audiomixer, Geräte Abfragen
- Mixer, Geräte Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038929"
---
# <a name="mixer-device-queries"></a>Geräte Abfragen im Mixer

Die Mixer-Dienste bieten Funktionen zum Bestimmen der Anzahl der im System vorhandenen mischunggeräte und der Funktionen der Geräte. Sie können auch eine Funktion "Mixer Dienste" verwenden, um den Geräte Bezeichner für ein Mischgerät zu ermitteln.

Sie können die Funktion " [**mixergetnumdecovs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) " verwenden, um zu bestimmen, wie viele Mixergeräte im System vorhanden sind. Mixergeräte werden anhand eines Geräte Bezeichners identifiziert. Geräte Bezeichner werden implizit von der Anzahl der Geräte, die in einem bestimmten System vorhanden sind, bestimmt. Sie reichen von 0 (null) bis zu der Anzahl der vorhandenen Geräte.

Vor der Verwendung eines Mixer-Geräts müssen Sie seine Funktionen bestimmen. Die Audiofunktionen können von einem Multimedia-Computer zu einem anderen unterschiedlich sein, sodass Anwendungen mit einer Vielzahl von Audiohardware arbeiten müssen.

Sie können die Funktion " [**mixergetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) " verwenden, um die Funktionen von mischergeräten zu bestimmen. Diese Funktion füllt eine [**mixercaps**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) -Struktur mit Informationen zu den Funktionen eines angegebenen Geräts.

Die [**mixergetid**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) -Funktion Ruft den dem angegebenen Geräte handle zugeordneten audiomischgeräterbezeichner ab. Beispielsweise können Sie mit dieser Funktion den Geräte Bezeichner für einen Audiomixer abrufen und dann mithilfe des Geräte Bezeichners das Volume anpassen oder ein anderes Steuerelement anzeigen.

 

 