---
title: Unterstützung für USB 3.0
description: Unterstützung für USB 3.0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca18cd9f38b17dfaa029738497cf93a43fd85477c9d3c5b30e83f506d5596e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671619"
---
# <a name="support-for-usb-30"></a>Unterstützung für USB 3.0

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

In Windows 8 und Windows Server 2012 haben wir Unterstützung für USB 3.0 hinzugefügt. Dazu wurde ein neuer Softwarestapel hinzugefügt, um den USB 3.0-Hostcontroller mit Strom zu betreiben, der als eXtensible Host Controller (XHC) bezeichnet wird. Wir haben Schnittstellenparität, IRQL-Ebene, Aufruferkontext, Fehlerstatus, Wiederholungshäufigkeit usw. beibehalten. Bei der Interaktion mit einem Gerät, das über USB 2.0 und USB 3.0 verbunden ist, sollte es keinen Unterschied geben.

Wenn Sie jedoch einen Treiber für ein neues USB 3.0-Gerät schreiben, entscheiden Sie sich definitiv für neue USB 3.0-Funktionen.

## <a name="manifestation"></a>Manifestation

Geräteübertragungen sind schneller, und usb-Geräte verbrauchen insgesamt weniger Strom von einem PC. Es besteht die Gefahr, dass vorhandene USB-Geräte möglicherweise nicht ordnungsgemäß funktionieren, wenn sie mit einem USB 3.0-Anschluss verbunden sind. Dies sollte nicht geschehen und ist nicht zu erwarten, aber da die Software, die USB 3.0 unterstützt, neu ist, ist dies ein Risiko.

 

 




