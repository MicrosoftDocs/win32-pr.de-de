---
title: Puffer Längen der Netzwerk Verwaltungsfunktion
description: In diesem Thema werden die Anforderungen für Funktions Puffer Längen bei der Verwendung mit den Netzwerkverwaltungs-APIs erörtert.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856232"
---
# <a name="network-management-function-buffer-lengths"></a>Puffer Längen der Netzwerk Verwaltungsfunktion

In diesem Thema werden die Anforderungen für Funktions Puffer Längen bei der Verwendung mit den Netzwerkverwaltungs-APIs erörtert.

Anwendungen, die beim Aufrufen der Enumerationsfunktionen für die Netzwerkverwaltung (und verschiedene Datenabruf Funktionen) Puffergrößen angeben, müssen Puffer angeben, die groß genug sind, um die zurückgegebene Informationsstruktur (oder Strukturen) sowie die Zeichen folgen, auf die ihre Elemente zeigen, aufzunehmen Wenn Sie keinen ausreichend großen Puffer angeben, um alle verfügbaren Einträge zu empfangen, gibt die Funktion Fehler \_ Weitere \_ Daten zurück. Enumerationsaufrufe geben keine partiellen Einträge zurück.

Einige Netzwerk Verwaltungsfunktionen verwenden einen richtlinienrichtlinienparameter mit der maximalen Daten Länge " *präfemaxlen*". Dieser Parameter ermöglicht es einer Anwendung, die Anzahl der Bytes vorzuschlagen, die der Server von einem Funktions Aufrufwert zurückgeben soll.

Wenn Sie im Parameter "präfemaxlen" den Wert "Max \_ Preferred length" angeben \_ , weisen die Netzwerk Verwaltungsfunktionen die Menge an Arbeitsspeicher zu, der für die Daten erforderlich ist. 

Weitere Informationen finden Sie unter [Netzwerk Verwaltungs Funktions Puffer](network-management-function-buffers.md).

 

 




