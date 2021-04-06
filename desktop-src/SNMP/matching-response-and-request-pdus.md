---
title: Übereinstimmende Antworten und Anforderungs-PDUs
description: Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, entspricht möglicherweise nicht der Reihenfolge, in der die Anwendung SNMP-Vorgangs Anforderungen übermittelt.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947893"
---
# <a name="matching-response-and-request-pdus"></a>Übereinstimmende Antworten und Anforderungs-PDUs

Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, entspricht möglicherweise nicht der Reihenfolge, in der die Anwendung SNMP-Vorgangs Anforderungen übermittelt. Damit die Antwort mit der Anforderung abgeglichen wird, muss die Anwendung das Feld Anforderungs- **ID (Anforderungs- \_ ID**) der Antwort verwenden.

Das Feld **Anforderungs- \_ ID** ist ein eindeutiger numerischer Wert, der das PDU identifiziert. Anwendungen können Anforderungs Bezeichner zuweisen, indem Sie die [**snmpcreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion oder die [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aufrufen. Rufen Sie die [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion auf, um eine PDU- **Anforderungs- \_ ID** abzurufen.

 

 




