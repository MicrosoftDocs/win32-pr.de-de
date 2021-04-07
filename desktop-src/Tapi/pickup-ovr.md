---
description: Der Pickup-Vorgang ermöglicht es einer Anwendung, eine Sitzung zu beantworten, bei der eine Warnung an einer anderen Adresse angezeigt wird. Die Anwendung identifiziert das Ziel der Abholung und gibt eine Sitzungs-ID für den aufzurufenden-Befehl zurück.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Aufhol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758335"
---
# <a name="pickup"></a>Aufhol

Der Pickup-Vorgang ermöglicht es einer Anwendung, eine Sitzung zu beantworten, bei der eine Warnung an einer anderen Adresse angezeigt wird. Die Anwendung identifiziert das Ziel der Abholung und gibt eine Sitzungs-ID für den aufzurufenden-Befehl zurück.

Es gibt mehrere Möglichkeiten, das Ziel der Abhol Anforderung zu identifizieren. Zuerst kann die Anwendung die Adresse der Warnungs Partei angeben. Zweitens: Wenn keine Adresse angegeben wird und der Switch dies zulässt, kann die Anwendung jede Warnungs Sitzung in der Pickup-Gruppe abrufen. Drittens ermöglichen einige Switches das Abfangen einer Sitzungs Warnung in einer anderen abholgruppe, wenn der Gruppen Bezeichner angegeben ist.

Einige Schlüssel Telefonsysteme unterstützen eine *Übertragung durch die Hold* -Funktion bei überbrückenden exklusiven anrufen. In diesem Schema besitzt ein bestimmtes Telefon einen Anruf exklusiv, wenn der Anruf aktiv ist, aber wenn der Anruf angehalten ist, kann jedes Telefon, das eine Darstellung der Linie aufweist, den Anruf aufnehmen.

**TAPI 2. x:** Eine Anwendung kann zu diesem Zweck einen Abholvorgang mit einer **null** -Zieladresse verwenden, ähnlich wie bei der Verwendung der Funktion zum Abrufen eines aufrufwartenden Aufrufens in einer analogen Zeile. Lineaddrfeature \_ pickbestätigte gibt an, dass die Funktion vorhanden ist.

Wenn lineaddrcapflags \_ pickupcallwait den Wert **true** hat, kann eine Sitzung übernommen werden, für die der Benutzer das aufrufende Signal, aber für das der Dienstanbieter die Erkennung nicht ausführen kann, übernommen hat. Dadurch erhält der Benutzer einen Mechanismus zum Beantworten eines wartenden Aufrufs, auch wenn der Dienstanbieter das Anruf Ende Signal nicht erkennen konnte. Sowohl die Zieladresse als auch die Gruppen-ID müssen **null** sein, um einen Rückruf aufzurufen.

Wenn eine Sitzung erfolgreich abgerufen wurde, empfängt die Anwendung eine Benachrichtigung über Statusänderungen, wobei der [Grund](reason-ovr.md) auf linecallreason Pickup festgelegt ist \_ .

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden [**Sie unter linepickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3. x:** Weitere Informationen finden [**Sie unter itbasiccallcontrol::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
