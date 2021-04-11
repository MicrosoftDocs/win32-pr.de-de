---
description: Geräteklassen vereinfachen die Entwicklung, da Programmierer Geräte, die ähnliche Eigenschaften haben, auf ähnliche Weise behandeln können.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Geräteklasse (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959719"
---
# <a name="device-class"></a>Geräteklasse

Geräteklassen vereinfachen die Entwicklung, da Programmierer Geräte, die ähnliche Eigenschaften haben, auf ähnliche Weise behandeln können. Beispielsweise verfügt ein digitales Telefon in einem Büro in der Regel über mehr Funktionen als ein Standard-Mobiltelefon in einem Zuhause, beide reagieren aber auf die gleiche Weise auf einen grundlegenden Satz von Funktionen, und beide gehören zu einer Mobiltelefon-Geräteklasse. Geräteklassen helfen, TAPI erweiterbar zu machen, indem Sie ein Framework bereitstellen, von dem neue Geräte klassifiziert und unterstützt werden.

Siehe [TAPI-Geräteklassen](./tapi-device-classes.md) für Klassen, die TAPI vordefiniert haben. Ein Dienstanbieter kann zusätzliche Geräteklassen für die von ihm unterstützten Geräte implementieren und definieren. Eine Anwendung muss nie wissen, welcher Dienstanbieter das Gerät steuert, aber möglicherweise Informationen zur Steuerung neuer Geräteklassen benötigt.

Ein Dienstanbieter implementiert eine Geräteklasse durch Zuordnung von Anforderungen zu tatsächlichen Geräte Befehlen. Wenn z. b. der Dienstanbieter für ein Hayes-kompatibles Modem einen Befehl empfängt, der durch TAPISVR an einen-Befehl übermittelt wird, sendet er klassische at-Befehle an das Modem.

Die Dienstanbieter Schnittstelle kann einer Vielzahl von Umgebungen zugeordnet werden, einschließlich derjenigen, die nicht üblicherweise als zu Telefonie gehörend betrachtet werden. Ein Beispiel hierfür sind multimediakkonferenzen über ein IP-basiertes Netzwerk, z. b. das Internet.

Anwendungsentwickler sollten das vorhanden sein anderer Anwendungen berücksichtigen, die möglicherweise Telefoniedienste gemeinsam nutzen.

 

 
