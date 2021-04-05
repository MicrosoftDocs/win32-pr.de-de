---
title: Der ADSI-Attribut Cache
description: Das ADSI-Objektmodell stellt einen Client seitigen Attribut Cache für jedes ADSI-Objekt bereit.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI-Attribut Cache ADSI
- ADSI ADSI, using, zugreifen auf und Bearbeiten von Daten mit ADSI, Attribut Cache
- Attribute ADSI, Attribut Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707374"
---
# <a name="the-adsi-attribute-cache"></a>Der ADSI-Attribut Cache

Das ADSI-Objektmodell stellt einen Client seitigen Attribut Cache für jedes ADSI-Objekt bereit. Der Attribut Cache ist mit einer Tabelle im Arbeitsspeicher vergleichbar, die die Namen und Werte der meisten Objekt Attribute enthält, die heruntergeladen wurden. Einige Attribute, z. b. operative Attribute, werden nicht zwischengespeichert. ADSI verwendet das Zwischenspeichern von Eigenschaften, um die Leistung der Attribut Manipulation zu verbessern und die Transaktions Funktion für Lese-und Schreibvorgänge von Attributen hinzuzufügen. Diese Funktion ist wichtig für Clients, die in Sprachen geschrieben wurden, die keinen systemeigenen Batch Verarbeitungs Mechanismus zum Festlegen von Attributen haben, wie z. b. Microsoft Visual Basic Development System. Ohne den ADSI-Eigenschafts Cache müssten diese Clients immer dann auf den Server zugreifen, wenn ein Attribut gelesen oder geschrieben wird.

Wenn ein Objekt erstellt oder zuerst an gebunden wird, ist der Eigenschafts Cache für das-Objekt leer. Wenn die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aufgerufen wird, lädt ADSI die angeforderten Attribute für das Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache. Wenn ein bestimmter Attribut Wert gelesen wird und der Cache leer ist, führt ADSI einen impliziten Rückruf der **IADs:: GetInfo** -Methode aus. Wenn der Cache ausgefüllt ist, funktionieren alle Attribut Lesevorgänge nur für den Inhalt des Caches.

Wenn ein Attribut Wert geschrieben wird, wird der neue Wert im lokalen Cache gespeichert, bis die [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) *-Methode aufgerufen wird. Wenn die **IADs::** *-Methode aufgerufen wird, werden die Attribute im Cache an den zugrunde liegenden Verzeichnisdienst übertragen. Nachdem die **IADs::** *-Methode aufgerufen wurde, verbleiben die Werte im Cache, bis Sie explizit mit einem weiteren Aufruf der [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aktualisiert werden.

> [!IMPORTANT]
> Die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode muss sorgfältig verwendet werden, da diese Methode immer die Attributwerte im Cache vom zugrunde liegenden Verzeichnisdienst überschreibt, auch wenn der zwischengespeicherte Wert geändert wurde. Das heißt, es werden Attributwerte überschrieben, die im Cache geändert wurden, aber nicht mit einem Commit der [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) *-Methode in den zugrunde liegenden Verzeichnisdienst committet wurden.

 

Die folgende Abbildung zeigt die verschiedenen Methoden, die für den Cache verwendet werden.

![ADSI-Attribut Cache](images/ds2propc.png)

 

 




