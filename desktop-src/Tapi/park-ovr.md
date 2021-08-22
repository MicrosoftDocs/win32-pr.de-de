---
description: Der Parkvorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, an der sie bis zum Unparking gehalten wird.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Park
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09067ad40bc965a6cd909d911de0070138e1d27addb552d728eff2ed60dde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335530"
---
# <a name="park"></a>Park

Der Parkvorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, an der sie bis zum Unparking gehalten wird. Aus Sicht der Anwendung sieht dies ähnlich wie eine Übertragung aus. Für die Partei am anderen Ende der Verbindung ähnelt dies dem Zurückhalten.

Der Unterschied zwischen Park und Übertragung besteht in der, dass die geparkte Adresse kein Verbindungspunkt für die Sitzung ist und die Sitzung keine Warnungen oder Time outs enthält. Der Unterschied zwischen Park und Hold besteht in der, dass die Sitzung nach Abschluss des Parkbetriebs nicht mehr mit der Adresse der Anwendung verknüpft ist.

Es werden zwei Formen des Parkens für eine Sitzung bereitgestellt: *Direktionalpark* und *nicht umgeleiteter Park.* In directed call park gibt die Anwendung die Zieladresse an, an der der Aufruf geparkt werden soll. Bei nicht direktionalen Parken bestimmt der Dienstanbieter oder die zugrunde liegende Hardware die Adresse und gibt sie an die Anwendung zurück.

Eine geparkte Sitzung geht in der Regel in den Leerlaufzustand über, nachdem sie erfolgreich geparkt wurde, und die Anwendung sollte dann die ihr zugeordneten Ressourcen frei geben. Eine [Zusammenfassung dazu finden Sie](terminate-a-session-ovr.md) unter Beenden einer Sitzung.

Wenn die Anwendung den Speicher für die Sitzung aufbelässt, werden neue Sitzungsressourcen auch dann zugeordnet, wenn die Anwendung die vorherigen Zeiger zurückgegeben hat, sodass ein Fehler bei ordnungsgemäßen Releases zu einer Vielzahl von Problemen führen kann.

Einige Dienstanbieter können den Benutzer daran erinnern, nachdem eine Sitzung für einen längeren Zeitraum geparkt wurde. Die Anwendung sieht einen Angebotsaufruf mit einem [Aufrufgrund, der](reason-ovr.md) auf "Reminder" festgelegt ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Siehe [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Weitere Informationen finden Sie unter [**ITBasicCallControl::P arkDirect,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect) [**ITBasicCallControl::P arkIndirect,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect) [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
