---
description: Mit dem Abholungsvorgang kann eine Anwendung eine Sitzung beantworten, die eine Warnung an einer anderen Adresse aussendet. Die Anwendung identifiziert das Ziel der Abholung und wird eine Sitzungs-ID für den abholten Anruf zurückgegeben.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Pickup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 288510d2d9e2eb2ed6e9a5cc5c58f6957b933b7d43db951eb330dd081a4c446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873060"
---
# <a name="pickup"></a>Pickup

Mit dem Abholungsvorgang kann eine Anwendung eine Sitzung beantworten, die eine Warnung an einer anderen Adresse aussendet. Die Anwendung identifiziert das Ziel der Abholung und wird eine Sitzungs-ID für den abholten Anruf zurückgegeben.

Es gibt mehrere Möglichkeiten, das Ziel der Abholungsanforderung zu identifizieren. Zunächst kann die Anwendung die Adresse der Warnungs partei angeben. Wenn keine Adresse angegeben ist und der Schalter dies zulässt, kann die Anwendung eine beliebige Warnungssitzung in ihrer Abholgruppe auswählen. Drittens ermöglichen einige Schalter die Abholung einer Sitzungswarnung in einer anderen Abholgruppe, wenn die Gruppen-ID angegeben ist.

Einige wichtige Telefonsysteme unterstützen eine *Übertragung über die Hold-Funktion* bei überbrückten exklusiven Anrufanrufen. In diesem Schema besitzt ein bestimmtes Telefon einen Anruf ausschließlich, wenn der Anruf aktiv ist, aber wenn der Anruf zurückbiert ist, kann jedes Telefon, das die Zeile anscheint, den Anruf aufrufen.

**TAPI 2.x:** Eine Anwendung kann zu diesem  Zweck einen Abholvorgang mit einer NULL-Zieladresse verwenden, ähnlich wie die -Funktion verwendet wird, um einen wartenden Anruf in einer analogen Zeile zu nutzen. LINEADDRFEATURE \_ PICKUPIERER gibt das Vorhandensein der Funktion an.

Wenn LINEADDRCAPFLAGS PICKUPCALLWAIT auf TRUE gesetzt ist, kann eine Sitzung verwendet werden, für die der Benutzer das Wartesignal für den Anruf erkannt hat, für die der Dienstanbieter die Erkennung jedoch nicht durchführen \_ kann.  Dadurch erhält der Benutzer einen Mechanismus zum Beantworten eines wartenden Anrufs, auch wenn der Dienstanbieter das Wartesignal für den Aufruf nicht erkennen konnte. Sowohl die Zieladresse als auch die Gruppen-ID müssen **NULL sein,** um einen Anruf mit Warteaufruf zu erhalten.

Wenn eine Sitzung erfolgreich empfangen wurde, erhält die Anwendung [](reason-ovr.md) eine Zustandsänderungsbenachrichtigung mit dem Grund, der auf LINECALLREASON PICKUP festgelegt \_ ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Weitere Informationen [**finden Sie unter linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3.x:** Weitere Informationen [**finden Sie unter ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
