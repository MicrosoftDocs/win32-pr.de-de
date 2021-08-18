---
title: Abbrechen der Neuübertragung
description: Wenn innerhalb des für eine Zielentität angegebenen Time outzeitraums keine Antwort auf eine Kommunikationsanforderung vorkommt und für die Entität Neuübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80770fc741357255adaa8b6bd15ab0e03b9148c37abf5fc631155d74b6d1f3a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009757"
---
# <a name="canceling-retransmission"></a>Abbrechen der Neuübertragung

Wenn innerhalb des für eine Zielentität angegebenen Time outzeitraums keine Antwort auf eine Kommunikationsanforderung vorkommt und für die Entität Neuübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut. Ein Aufruf der [**SnmpCancelMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) kann diesen Neuübertragungszyklus abbrechen und interne Datenstrukturen frei geben, die der Nachrichtenanforderung zugeordnet sind.

Beachten Sie, dass eine Zielentität eine SNMP-Nachricht empfangen kann, die durch einen Aufruf der [**SnmpCancelMsg-Funktion abgebrochen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) wurde. Es ist auch möglich, dass eine Zielentität auf eine abgebrochene SNMP-Nachricht reagieren kann. Dies liegt daran, dass Transaktionswarteschlangen auf mehreren Ebenen auftreten. Nachdem eine Nachricht jedoch durch einen Aufruf von [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)abgebrochen wurde, überträgt die Microsoft WinSNMP-Implementierung die Nachricht nicht erneut, übermittelt keine Antwort-PDU oder sendet keine Time outbenachrichtigung für diese Nachricht an die Anwendung.

 

 




