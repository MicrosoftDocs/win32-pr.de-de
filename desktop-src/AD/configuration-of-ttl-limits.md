---
title: Konfiguration von TTL-Grenzwerten
description: Ein Client kann einen TTL-Wert für einen Eintrag im Bereich zwischen 1 und 31557600 anfordern (d. b. zwischen 1 Sekunde und 1 Jahr).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Konfiguration von TTL-Grenzwerten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881605"
---
# <a name="configuration-of-ttl-limits"></a>Konfiguration von TTL-Grenzwerten

Ein Client kann einen TTL-Wert für einen Eintrag im Bereich zwischen 1 und 31557600 anfordern (d. b. zwischen 1 Sekunde und 1 Jahr). Dieser Attributwertbereich wird von den **RangeLower-** und **rangeUpper-Attributwerten** in der **attributeSchema-Definition** für das **entryTTL-Attribut** erzwungen. Gemäß RFC 2589 müssen Verzeichnisserver diesen Wert nicht akzeptieren und geben möglicherweise einen anderen TTL-Wert an den Client zurück. Clients müssen in der Lage sein, diesen vom Server vorgegebenen Wert als Clientaktualisierungszeitraum (CRP) zu verwenden, der bestimmt, wie oft der Client den Aktualisierungsvorgang für den dynamischen Eintrag ausführen muss.

Active Directory Domain Services Administratoren die Möglichkeit bieten, die Standard- und Mindestwerte für die Gültigkeitsdauer für eine Gesamtstruktur zu konfigurieren. Der TTL-Standardwert wird einem neu erstellten dynamischen Eintrag zugewiesen, wenn eine Gültigkeitsdauer nicht explizit angegeben wird. Die minimale Gültigkeitsdauer überschreibt alle vom Client angegebenen TTL-Werte, die niedriger als der konfigurierte Mindestwert sind. Es muss kein konfigurierbarer maximaler TTL-Wert angegeben werden, da ein Maximum durch den **rangeUpper-Attributwert** im **attributeSchema-Objekt** vorgegeben wird. Wenn Administratoren diese Werte konfigurieren können, können sie TTL-Werte festlegen, die einen geringen Aktualisierungsdatenverkehr erzwingen oder im anderen Extremfall ein äußerst aktuelles Verzeichnis bereitstellen.

Die Standardwerte für die beiden konfigurierbaren TTL-Parameter sind wie folgt:

-   TTL-Standardwert = 86.400 Sekunden (1 Tag)
-   TTL-Mindestwert = 900 Sekunden (15 Minuten)

Die konfigurierbaren TTL-Parameter werden als AVA-Einträge (Attributwertassertion) im &lt; Format "Wertname-Wert" &gt; = &lt; im Attribut &gt; **ms-DS-Other-Einstellungen** des NTDS-Service Objekts gespeichert, das vom folgenden DN in der Konfigurationspartition angegeben wird:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



Die genaue AVA-Syntax für die beiden konfigurierbaren TTL-Parameter lautet wie folgt, wobei NNNN in Sekunden ausgedrückt wird:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Diese Werte können von einem Administrator über das Befehlszeilenprogramm ntdsutil festgelegt werden.

 

 




