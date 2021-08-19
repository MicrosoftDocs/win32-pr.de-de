---
title: Adsi-Attributcache
description: Das ADSI-Objektmodell stellt einen clientseitigen Attributcache für jedes ADSI-Objekt bereit.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI-Attributcache ADSI
- ADSI ADSI , Verwenden, Zugreifen auf und Bearbeiten von Daten mit ADSI, Attributcache
- Attribute ADSI , Attributzwischenspeicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5940d431fc476fdecd8397875bf06a04ed82ea30ab4ed2e98b94ccef98f0e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930045"
---
# <a name="the-adsi-attribute-cache"></a>Adsi-Attributcache

Das ADSI-Objektmodell stellt einen clientseitigen Attributcache für jedes ADSI-Objekt bereit. Der Attributcache ist vergleichbar mit einer Tabelle im Arbeitsspeicher, die die Namen und Werte der meisten heruntergeladenen Objektattribute enthält. Einige Attribute, z. B. Betriebsattribute, werden nicht zwischengespeichert. ADSI verwendet das Zwischenspeichern von Eigenschaften, um die Leistung der Attributbearbeitung zu verbessern und Transaktionsfunktionen für Lese- und Schreibvorgänge von Attributen hinzuzufügen. Diese Funktion ist wichtig für Clients, die in Sprachen geschrieben wurden und über keinen nativen Batchverarbeitungsmechanismus zum Festlegen von Attributen verfügen, z. B. Microsoft Visual Basic Entwicklungssystem. Ohne den ADSI-Eigenschaftencache müssten solche Clients jedes Mal auf den Server zugreifen, wenn ein Attribut gelesen oder geschrieben wird.

Wenn ein Objekt erstellt oder zum ersten Mal an gebunden wird, ist der Eigenschaftencache für das Objekt leer. Wenn die [**IADs::GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) aufgerufen wird, lädt ADSI die angeforderten Attribute für das Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache. Wenn ein bestimmter Attributwert gelesen wird und der Cache leer ist, führt ADSI einen impliziten Aufruf der **IADs::GetInfo-Methode** aus. Wenn der Cache gefüllt ist, funktionieren alle Attributlesevorgänge nur für den Inhalt des Caches.

Wenn ein Attributwert geschrieben wird, wird der neue Wert im lokalen Cache gespeichert, bis die [**IADs::SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufgerufen wird. Wenn die **IADs::SetInfo-Methode** aufgerufen wird, werden die Attribute im Cache an den zugrunde liegenden Verzeichnisdienst übertragen. Nachdem die **IADs::SetInfo-Methode** aufgerufen wurde, verbleiben die Werte im Cache, bis sie explizit mit einem anderen Aufruf der [**IADs::GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) aktualisiert werden.

> [!IMPORTANT]
> Die [**IADs::GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) muss sorgfältig verwendet werden, da diese Methode immer die Attributwerte im Cache aus dem zugrunde liegenden Verzeichnisdienst überschreibt, auch wenn der zwischengespeicherte Wert geändert wurde. Das heißt, es überschreibt Attributwerte, die im Cache geändert wurden, aber nicht mit einem Aufruf der [**IADs::SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) an den zugrunde liegenden Verzeichnisdienst übergeben werden.

 

Die folgende Abbildung zeigt die verschiedenen Methoden, die für den Betrieb im Cache verwendet werden.

![adsi-Attributcache](images/ds2propc.png)

 

 




