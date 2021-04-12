---
title: Regdsapi. CPP
description: In der Beispiel Anbieter Komponente sind Funktionen, die eine API darstellen, die direkt auf das native Betriebssystem zugreift, in regdsapi. cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309228"
---
# <a name="regdsapicpp"></a>Regdsapi. CPP

In der Beispiel Anbieter Komponente sind Funktionen, die eine API darstellen, die direkt auf das native Betriebssystem zugreift, in regdsapi. cpp. Die Beispiel Anbieter Komponente implementiert ihren Verzeichnisdienst in der Registrierung. Um einen Anbieter zu schreiben, der auf Ihren eigenen Verzeichnisdienst zugreift, erstellen Sie Ihre eigenen Implementierungen dieser API. Die unterstützten Funktionen sind in der folgenden Tabelle aufgeführt.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sampledsopenobject**             | Öffnen Sie dieses Objekt nach dem Namen. Wenn der Schema-Klassentyp Parameter **null** ist, füllen Sie den gefundenen Typ aus. Ruft ein Handle für das-Objekt ab.                                                             |
| **Sampledscloseobject**            | Verwenden Sie das Handle, das von **sampledsopenobject** abgerufen wurde.                                                                                                                                            |
| **Sampledsrdnerum**                | Rufen Sie das Handle für ein Enumeratorobjekt ab, um die Enumeration von relativen Distinguished Names (rDNS) aus einem Container Objekt zu verwalten.                                                          |
| **Sampledsnextrdn**                | Wenn Sie das von **sampledsrdnenum** abgerufene Handle verwenden, erhalten Sie den nächsten relativen Distinguished Name aus diesem Container Objekt.                                                                        |
| **Sampledsfreaufumum**               | Gibt das in **sampledsrdnenum** zugewiesene Enumeratorobjekt frei.                                                                                                                                   |
| **Sampledsmodifyobject**           | Ändern Sie die Eigenschaften eines Objekts im Verzeichnisdienst mit dem Handle des Objekts und einer Liste von Attributen und deren Werten.                                                              |
| **Sampledsread Object**             | Lesen Sie die Eigenschaften des Objekts aus dem Verzeichnisdienst. Ordnen Sie die Syntax aus dem systemeigenen Speicher den entsprechenden ADS-Syntax Werten zu. Behandeln Sie Eigenschaften mit mehreren Werten entsprechend. |
| **Sampledsgetpropertydefinition**  | Suchen Sie im Schema nach allen Eigenschafts Definitionen und deren Attributen für diesen Typ von Schema Klassen Objekten.                                                                                     |
| **Sampledsgetpropertydefinition**  | Suchen Sie im Schema diese Eigenschaft und deren Attribute nach Namen.                                                                                                                               |
| **Sampledsfrepropertydefinition** | Der von **getpropertydefinition** zugeordnete Arbeitsspeicher wird freigegeben.                                                                                                                                            |
| **Sampledsgettypintext**            | Get the Schema Class Type of a Object in Textformat.                                                                                                                                         |
| **Sampledsgettype**                | Get the Schema Class Type of a Object.                                                                                                                                                        |
| **Sampledsgetpropertyinfo**        | Wenn ein Handle für das Schema Klassenobjekt und einen Eigenschaftsnamen gegeben ist, rufen Sie die Eigenschafts Informationen wie Syntax usw. ab.                                                                      |
| **FreeList**                       | Freigeben des von einer LPWSTR-Liste verwendeten Speichers \_ .                                                                                                                                                        |
| **Sampledsgetclassdefinition**     | Rufen Sie den Satz aller Schema Klassendefinitionen und der zugehörigen Daten aus dem Schema ab.                                                                                                    |
| **Sampledsgetclassdefinition**     | Abrufen von Daten über eine bestimmte Schema Klasse im Schema.                                                                                                                                   |
| **Sampledsgetclassinfo**           | Nach dem Namen einer Schema Klasse suchen Sie die zugehörigen Daten, wie z. b. obligatorische Eigenschaften.                                                                                                      |
| **Sampledsaddobject**              | Fügen Sie ein Objekt im Verzeichnisdienst hinzu.                                                                                                                                                        |
| **Sampledsremoveobject**           | Entfernen Sie ein Objekt aus dem Verzeichnisdienst.                                                                                                                                                   |
| **Sampledscreatebuffer**           | Erstellen Sie einen Arbeitsspeicher Puffer für Attributdaten und Vorgangs Daten.                                                                                                                                  |
| **Sampledsfrebuffer**             | Freigeben des Puffers, der in **sampledscreatebuffer** erstellt wurde.                                                                                                                                           |



 

 

 




