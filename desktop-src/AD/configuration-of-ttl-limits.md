---
title: Konfiguration von TTL-Limits
description: Ein Client kann einen TTL-Wert für einen Eintrag im Bereich von 1 bis 31557600 (d. h. von 1 Sekunde bis 1 Jahr) anfordern.
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Konfiguration der TTL-Grenzwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707194"
---
# <a name="configuration-of-ttl-limits"></a>Konfiguration von TTL-Limits

Ein Client kann einen TTL-Wert für einen Eintrag im Bereich von 1 bis 31557600 (d. h. von 1 Sekunde bis 1 Jahr) anfordern. Dieser Attributwerte Bereich wird von den **rangeLower** -und **rangeUpper** -Attributwerten in der **attributeSchema** -Definition für das **entryttl** -Attribut erzwungen. Gemäß RFC 2589 müssen Verzeichnisserver diesen Wert nicht akzeptieren, und es wird möglicherweise ein anderer TTL-Wert an den Client zurückgegeben. Clients müssen diesen vom Server vorgegebenen Wert als Client Aktualisierungs Zeitraum (CRP) verwenden können, mit dem bestimmt wird, wie oft der Client den Aktualisierungs Vorgang für den dynamischen Eintrag ausführen muss.

Active Directory Domain Services Administratoren die Möglichkeit bieten, die Standard-und die minimalen TTL-Werte für eine Gesamtstruktur zu konfigurieren. Der Standardwert für die Gültigkeitsdauer wird einem neu erstellten dynamischen Eintrag zugewiesen, wenn eine Gültigkeitsdauer nicht explizit angegeben wird. Die minimale Gültigkeitsdauer überschreibt jeden vom Client angegebenen TTL-Wert, der niedriger ist als der konfigurierte Mindestwert. Es muss kein konfigurierbarer maximaler TTL-Wert angegeben werden, da ein Maximum durch den Wert des **rangeUpper** -Attributs im **attributeSchema** -Objekt festgelegt wird. Wenn Sie zulassen, dass Administratoren diese Werte konfigurieren, können Sie TTL-Werte festlegen, die einen niedrigen Aktualisierungs Datenverkehr erzwingen, oder auf der anderen Seite ein hoch aktuellste Verzeichnis bereitstellen.

Die Standardwerte für die zwei konfigurierbaren TTL-Parameter lauten wie folgt:

-   Standardmäßiger TTL-Wert = 86400 Sekunden (1 Tag)
-   Minimaler TTL-Wert = 900 Sekunden (15 Minuten)

Die konfigurierbaren TTL-Parameter werden als AVA-Einträge (Attribut Wert Assertionen) in der Form "<-Wertname>=" gespeichert.<value>"im Attribut **ms-DS-Other-Settings** des NTDS-Service Objekts, das durch den folgenden DN in der Konfigurations Partition angegeben wird:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



Die exakte AVA-Syntax für die zwei konfigurierbaren TTL-Parameter ist wie folgt, wobei nnnn in Sekunden ausgedrückt wird:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Diese Werte können von einem Administrator über das Befehlszeilen-Hilfsprogramm Ntdsutil festgelegt werden.

 

 




