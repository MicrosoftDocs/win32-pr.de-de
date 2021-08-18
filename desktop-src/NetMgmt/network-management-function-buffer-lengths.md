---
title: Pufferlängen der Netzwerkverwaltungsfunktion
description: In diesem Thema werden die Anforderungen für Funktionspufferlängen erläutert, wenn sie mit den Netzwerkverwaltungs-APIs verwendet werden.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858b01de7b0b4cecb9eaea9f93bb541cb95fe9b394e74616427910abe3b33403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911740"
---
# <a name="network-management-function-buffer-lengths"></a>Pufferlängen der Netzwerkverwaltungsfunktion

In diesem Thema werden die Anforderungen für Funktionspufferlängen erläutert, wenn sie mit den Netzwerkverwaltungs-APIs verwendet werden.

Anwendungen, die beim Aufrufen von Enumerationsfunktionen für die Netzwerkverwaltung Puffergrößen angeben (und verschiedene Datenabruffunktionen), müssen Puffer angeben, die groß genug sind, um die zurückgegebene Informationsstruktur (oder -strukturen) sowie die Zeichenfolgen zu enthalten, auf die ihre Member zeigen. Wenn Sie keinen ausreichend großen Puffer angeben, um alle verfügbaren Einträge zu empfangen, gibt die Funktion ERROR \_ MORE \_ DATA zurück. Enumerationsaufrufe geben keine partiellen Einträge zurück.

Einige Netzwerkverwaltungsfunktionen verwenden den Parameter *prefmaxlen* für die maximale Datenlänge. Mit diesem Parameter kann eine Anwendung die Anzahl der Bytes vorschlagen, die der Server von einem Funktionsaufruf zurückgeben soll.

Wenn Sie den Wert MAX \_ PREFERRED \_ LENGTH im *prefmaxlen-Parameter* angeben, ordnen die Netzwerkverwaltungsfunktionen den für die Daten erforderlichen Arbeitsspeicher zu.

Weitere Informationen finden Sie unter [Netzwerkverwaltungsfunktionspuffer.](network-management-function-buffers.md)

 

 




