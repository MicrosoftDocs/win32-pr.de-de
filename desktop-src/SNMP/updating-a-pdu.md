---
title: Aktualisieren eines PDU
description: Eine WinSNMP-Anwendung kann ausgewählte PDU-Felder mithilfe der snmpgetpdudata-Funktion und der snmpsetpdudata-Funktion abrufen und aktualisieren.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713337"
---
# <a name="updating-a-pdu"></a>Aktualisieren eines PDU

Eine WinSNMP-Anwendung kann ausgewählte PDU-Felder mithilfe der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion und der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion abrufen und aktualisieren.

Die Anwendung kann die Felder "PDU", "Anforderungs Bezeichner", "Fehlerstatus" und "Fehler index" von einem bestimmten PDU abrufen. Außerdem kann das Handle für die Variablen Bindungs Liste abgerufen werden. Die Anwendung kann die Felder **PDU- \_ Typ** und **Anforderungs- \_ ID** aktualisieren.

Wenn der PDU-Typ gleich SNMP \_ PDU \_ Getbulk ist, kann die Anwendung auch die **nicht \_ Wiederhol** enden und die Felder für die **Maximale \_ Wiederholung** des PDU-Vorgangs aktualisieren.

 

 




