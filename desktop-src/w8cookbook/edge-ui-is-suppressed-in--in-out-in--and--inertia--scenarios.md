---
title: Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.
description: Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207315"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.

## <a name="platform"></a>Plattform

<dl> Clients-Windows 8.1  
</dl>

## <a name="description"></a>BESCHREIBUNG

In einigen Fällen kann es vorkommen, dass Benutzer versehentlich Edge-UI aufrufen (Charms, App-Leiste, App-Wechsel). Wir haben eine Funktion eingeführt, die es Entwicklern ermöglicht, Ihre Benutzeroberfläche für den gesamten Bildschirm zu entwerfen, ohne dass Sie eine Fülle (z. b. Rahmen) erstellen müssen, um zu verhindern, dass der Benutzer versehentlich die Ränder

Es gibt zwei Fälle, die in den meisten Fällen dazu führen können, dass unbeabsichtigte Kanten geroutete Kanten entstehen:

-   Beim schnellen schwenken können die Geschwindigkeit und die Ungenauigkeit der Interaktion gelegentlich bewirken, dass Sie vom Bildschirmrand ausgehen.
-   Wenn Benutzer den Bildschirmbereich beim Binden mit dem Finger, z. b. in einer Zeichnungs-APP, schnell verlassen und erneut eingeben, kann dieses Voreingegebene Verhalten versehentlich die Edge-Benutzeroberfläche auslöst und die Benutzeroberfläche unterbrechen.

Um die Benutzer-und Entwickler Oberfläche zu verbessern, wird die Edge-Benutzeroberfläche nun in zwei bestimmten Instanzen unterdrückt:

-   Wenn ein Benutzer in einer Anwendung, die dmanip-Trägheit unterstützt und während der Trägheit auftritt, auf den Bildschirm zeigt, wird die Edge-Benutzeroberfläche nicht innerhalb eines Timeout Fensters aufgerufen.
-   Auf zertifizierten Geräten wird die Edge-Benutzeroberfläche nicht aufgerufen, wenn ein Benutzer innerhalb bestimmter Parameter schnell vom Bildschirm auf den Bildschirm außerhalb des Bildschirms und wieder in (in-out-of-Motion) aufzieht.

## <a name="manifestations"></a>Kundgebungen

Benutzer können schnell auf den Rand schwenken, während bei der Verwendung einer App eine Abnahme des unbeabsichtigten Edge-Aufforderungen angezeigt wird.

## <a name="solution"></a>Lösung

Entwickler sollten diese entschärfungen berücksichtigen und sollten in der Lage sein, den Vollbildmodus zu verwenden, ohne zu befürchten, dass Benutzer bei der Interaktion mit der Anwendung auf dem Edge versehentlich die Edge-Benutzeroberfläche auslöst.

 

 




