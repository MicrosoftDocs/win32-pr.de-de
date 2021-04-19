---
description: Andere TAPI-Telefonfunktionen verwenden ein Handle für ein geöffnetes Telefongerät, um das geöffnete Telefongerät zu identifizieren.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: Geräte-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348404"
---
# <a name="device-ids"></a>Geräte-IDs

Andere TAPI-Telefonfunktionen verwenden ein Handle für ein geöffnetes Telefongerät, um das geöffnete Telefongerät zu identifizieren. Die einzigen Funktionen für Telefongeräte, die einen Parameter für einen Telefongeräte Bezeichner verwenden (im Gegensatz zu einem Telefon handle), sind die [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) -und [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) -Funktionen. Eine Anwendung kann den Geräte Bezeichner des Telefons abrufen, indem er die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion mit dem Telefon Handle als Parameter verwendet.

Eine Anwendung kann auch Geräte Bezeichner für verschiedene Geräteklassen abrufen, die einem geöffneten Telefon zugeordnet sind, indem [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)aufgerufen wird. Weitere Informationen finden Sie unter [TAPI-Geräteklassen](tapi-device-classes.md) für Geräteklassen Namen.

Diese Funktion nimmt einen Telefon Handle und eine Beschreibung der Geräteklasse an. Er gibt den Geräte Bezeichner für das Gerät der angegebenen Geräteklasse zurück, die dem geöffneten Telefongerät zugeordnet ist. Wenn die Geräteklasse "TAPI/Phone" ist, wird der Geräte Bezeichner des Telefon Geräts zurückgegeben.

Im Gegensatz zu Linien Geräten, für die die grundlegenden Zeilen Dienste die Entsprechung von Töpfen bereitstellen, wird für Telefongeräte kein minimal garantierter Satz von Funktionen definiert. Obwohl jedes Telefongerät mindestens die in diesem Abschnitt beschriebenen Funktionen und Nachrichten bereitstellt, bieten Sie keine tatsächlichen Vorgänge auf dem physischen Telefongerät an.

 

 



