---
title: Übereinstimmende Antwort- und Anforderungs-PDUs
description: Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, stimmt möglicherweise nicht mit der Reihenfolge überein, in der die Anwendung SNMP-Vorgangsanforderungen übermittelt.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009318"
---
# <a name="matching-response-and-request-pdus"></a>Übereinstimmende Antwort- und Anforderungs-PDUs

Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, stimmt möglicherweise nicht mit der Reihenfolge überein, in der die Anwendung SNMP-Vorgangsanforderungen übermittelt. Um die Antwort mit der Anforderung abzugleichen, muss die Anwendung das Anforderungsbezeichnerfeld (die **\_ Anforderungs-ID)** der Antwort verwenden.

Das **\_ Anforderungs-ID-Feld** ist ein eindeutiger numerischer Wert, der die PDU identifiziert. Anwendungen können Anforderungsbezeichner zuweisen, indem sie die [**SnmpCreatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) oder die [**SnmpSetPduData-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) aufrufen. Rufen Sie die [**SnmpGetPduData-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) auf, um die **\_ Anforderungs-ID** eines PDU abzurufen.

 

 




