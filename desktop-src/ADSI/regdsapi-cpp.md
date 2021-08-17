---
title: REGDSAPI. Cpp
description: In der Beispielanbieterkomponente befinden sich Funktionen, die eine API darstellen, die direkt auf das native Betriebssystem zuzugreifen, in Regdsapi.cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80179650c51f3561b8ab73bb5b28cd428867f7feac79a8341b315a1f2a510d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307660"
---
# <a name="regdsapicpp"></a>REGDSAPI. Cpp

In der Beispielanbieterkomponente befinden sich Funktionen, die eine API darstellen, die direkt auf das native Betriebssystem zuzugreifen, in Regdsapi.cpp. Die Beispielanbieterkomponente implementiert ihren Verzeichnisdienst in der Registrierung. Um einen Anbieter zu schreiben, der auf Ihren eigenen Verzeichnisdienst zuzugreifen, erstellen Sie Ihre eigenen Implementierungen dieser API. Die unterstützten Funktionen sind in der folgenden Tabelle aufgeführt.



| Methode                             | Beschreibung                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Öffnen Sie dieses Objekt nach Namen. Wenn der Typparameter der Schemaklasse **NULL ist,** geben Sie den gefundenen Typ ein. Ruft ein Handle für das -Objekt ab.                                                             |
| **SampleDSCloseObject**            | Verwenden Sie das von **SampleDSOpenObject abgerufene Handle.**                                                                                                                                            |
| **SampleDSRDNEnum**                | Rufen Sie das Handle für ein Enumeratorobjekt ab, um die Enumeration relativer Distinguished Names (RDNs) aus einem Containerobjekt zu verwalten.                                                          |
| **SampleDSNextRDN**                | Rufen Sie mithilfe des von **SampleDSRDNEnum abgerufenen** Handles den nächsten relativen Distinguished Name aus diesem Containerobjekt ab.                                                                        |
| **SampleDSFreeEnum**               | Geben Sie das in **SampleDSRDNEnum** zugeordnete Enumeratorobjekt frei.                                                                                                                                   |
| **SampleDSModifyObject**           | Ändern Sie die Eigenschaften eines Objekts im Verzeichnisdienst, indem Sie das Handle des Objekts und eine Liste von Attributen und deren Werten angeben.                                                              |
| **SampleDSReadObject**             | Liest die Eigenschaften des Objekts aus dem Verzeichnisdienst. Ordnen Sie die Syntax aus dem nativen Speicher den entsprechenden ADS-Syntaxwerten zu. Behandeln Sie Eigenschaften mit mehreren Werten entsprechend. |
| **SampleDSGetPropertyDefinition**  | Suchen Sie im Schema alle Eigenschaftendefinitionen und deren Attribute für diesen Typ von Schemaklassenobjekt.                                                                                     |
| **SampleDSGetPropertyDefinition**  | Suchen Sie im Schema nach dieser Eigenschaft und ihren Attributen nach Namen.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Freier Speicher, der von **GetPropertyDefinition zugeordnet wird.**                                                                                                                                            |
| **SampleDSGetTypeText**            | Gibt den Schemaklassentyp eines Objekts im Textformat an.                                                                                                                                         |
| **SampleDSGetType**                | Gibt den Schemaklassentyp eines Objekts an.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Rufen Sie bei einem Handle für das Schemaklassenobjekt und einem Eigenschaftennamen die Eigenschaftsinformationen ab, z. B. Syntax und so weiter.                                                                      |
| **FreeList**                       | Geben Sie den von einer LPWSTR LIST verwendeten Arbeitsspeicher \_ frei.                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Ruft den Satz aller Schemaklassendefinitionen und der zugehörigen Daten aus dem Schema ab.                                                                                                    |
| **SampleDSGetClassDefinition**     | Ruft Daten zu einer bestimmten Schemaklasse im Schema ab.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Suchen Sie mit dem Namen einer Schemaklasse nach den zugehörigen Daten, z. B. obligatorischen Eigenschaften.                                                                                                      |
| **SampleDSAddObject**              | Fügen Sie dem Verzeichnisdienst ein -Objekt hinzu.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Entfernen Sie ein Objekt aus dem Verzeichnisdienst.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Erstellen Sie einen Speicherpuffer für Attributdaten und Vorgangsdaten.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Geben Sie den in **SampleDSCreateBuffer erstellten Puffer frei.**                                                                                                                                           |



 

 

 




