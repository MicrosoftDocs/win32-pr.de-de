---
description: Das Aufruf Objekt stellt eine adressieren-Verbindung zwischen der lokalen Adresse und mindestens einer anderen Adresse dar.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Calltobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363851"
---
# <a name="call-object"></a>Calltobjekt

Das "Callcenter"-Objekt stellt die Verbindung einer Adresse zwischen der lokalen Adresse und einer oder mehreren anderen Adressen dar. Alle callensteuerelemente werden über das-Objekt aufgerufen. [**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) und [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sind die am häufigsten verwendeten Schnittstellen des Aufruf Objekts. Diese Schnittstellen implementieren eine Reihe von Vorgängen und Abfragen, z. b. das Abrufen von Schnittstellen Zeigern für Medienströme oder das Abrufen der Aufruferkennung Weitere Informationen zu [Sitzungs Vorgängen](session-operations-ovr.md) und [Sitzungsinformationen](session-information-ovr.md) finden Sie in den Abschnitten Haupt Übersicht über die von TAPI unterstützten Überprüfungen.

Ein Medien Dienstanbieter kann [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)implementieren, die auf einem calltobjekt von TAPI aggregiert werden. Ausführliche Informationen zu den von einem Anbieter implementierten Informationen finden Sie in der Dokumentation des Dienstanbieters.

Die Beispiele zum Ausführen [eines aufrufscodes](make-a-call.md) und zum [empfangen eines Aufrufcodes](receive-a-call.md) veranschaulichen einige Abbildungen der Verwendung eines calltobjekt.

Eine Liste aller dem-Objekt zugeordneten Schnittstellen finden Sie unter [Callcenter-Schnittstellen](call-object-interfaces.md) .

 

 



