---
description: Der Park-Vorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, in der Sie bis zum Entsperren aufbewahrt wird.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Wildpark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349879"
---
# <a name="park"></a>Wildpark

Der Park-Vorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, in der Sie bis zum Entsperren aufbewahrt wird. Aus Sicht der Anwendung sieht dies wie eine Übertragung aus. Der Partei am anderen Ende der Verbindung ähnelt dies dem ablegen.

Der Unterschied zwischen Park und Transfer besteht darin, dass die geparkte Adresse kein Verbindungspunkt für die Sitzung ist, und die Sitzung nicht benachrichtigt wird oder ein Timeout auftritt. Der Unterschied zwischen Park und Hold besteht darin, dass die Sitzung nicht mehr mit der Adresse der Anwendung verknüpft ist, sobald der Park Vorgang abgeschlossen ist.

Zwei Arten von Parken einer Sitzung werden bereitgestellt: der *gesteuerte Park* und der *nicht gesteuerte Park*. In einem gerichteten callpark gibt die Anwendung die Zieladresse an, in der der-Befehl geparkt werden soll. Bei einem nicht gesteuerten Park ermittelt der Dienstanbieter oder die zugrunde liegende Hardware die Adresse und gibt Sie an die Anwendung zurück.

Eine geparierte Sitzung wechselt in der Regel in den Leerlaufzustand, nachdem Sie erfolgreich geparkt wurde, und die Anwendung sollte dann die ihr zugeordneten Ressourcen freigeben. Eine Zusammenfassung der Vorgehensweise finden Sie unter [Beenden einer Sitzung](terminate-a-session-ovr.md) .

Wenn die Anwendung die Sitzung entbindet, werden neue Sitzungs Ressourcen zugewiesen, selbst wenn die Anwendung die vorherigen Zeiger zurückgegeben hat, sodass das Ausführen von ordnungsgemäßen Releases zu einer Vielzahl von Problemen führen kann.

Einige Dienstanbieter können den Benutzer erinnern, nachdem eine Sitzung für einen längeren Zeitraum geparkt wurde. Die Anwendung sieht einen Angebots-und einen Anforderungstyp, der auf [Erinnerung festgelegt](reason-ovr.md) ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linepark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineunpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Siehe [**itbasiccallcontrol::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**itbasiccallcontrol::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**itbasiccallcontrol:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
