---
description: Netzwerkmonitor enthält die folgenden BLOB-Funktionen.
ms.assetid: 90514067-59e9-4bd9-8612-2263bd414574
title: BLOB-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a059e997a06d3295f598d65956c62d06953767ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348592"
---
# <a name="blob-functions"></a>BLOB-Funktionen

Netzwerkmonitor enthält die folgenden BLOB-Funktionen.



| Funktion                                                       | BESCHREIBUNG                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [CreateBlob](createblob.md)                                   | Erstellt ein leeres BLOB.                                                                                                           |
| ["Kreatenppinterface"](createnppinterface.md)                   | Erstellt eine NPP-Schnittstelle mit einem angegebenen BLOB.                                                                                      |
| [Destroyblob](destroyblob.md)                                 | Gibt den gesamten Arbeitsspeicher frei, der einem angegebenen BLOB zugeordnet ist.                                                                                   |
| [Duplicateblob](duplicateblob.md)                             | Kopiert ein bestimmtes Blob.                                                                                                             |
| [Getboolfromblob](getboolfromblob.md)                         | Ruft den benannten booleschen Wert aus einem angegebenen BLOB ab.                                                                             |
| [Getclassidfromblob](getclassidfromblob.md)                   | Ruft den Wert des benannten Klassen Bezeichners aus einem angegebenen BLOB ab.                                                                    |
| [Getdwordfromblob](getdwordfromblob.md)                       | Ruft den benannten **DWORD** -Wert aus einem angegebenen BLOB ab.                                                                           |
| [Getmacaddressfromblob](getmacaddressfromblob.md)             | Ruft die benannte Mac-Adresse aus einem angegebenen BLOB ab.                                                                               |
| [Getnetworkinfofromblob](getnetworkinfofromblob.md)           | Ruft Netzwerkinformationen von einem angegebenen BLOB ab.                                                                                 |
| [Getnppaddressfilterfromblob](getnppaddressfilterfromblob.md) | Ruft Adress Filter Informationen aus einem angegebenen BLOB ab.                                                                          |
| [Getnppblobfromui](getnppblobfromui.md)                       | Zeigt das Dialogfeld **Netzwerk auswählen** an und gibt das NPP-BLOB der ausgewählten NIC zurück.                                       |
| [Getnppblobtable](getnppblobtable.md)                         | Ruft eine Tabelle mit blobspeicher ab.                                                                                                      |
| [Getnpettypesapfilter](getnppetypesapfilter.md)               | Ruft den ETYPE/SAP-Filter aus einem angegebenen BLOB ab.                                                                                |
| [Getnppmactybäuernumber](getnppmactypeasnumber.md)             | Ruft den Mac-Typ aus der Kategorie **networkinfo** des NPP-Abschnitts ab und konvertiert die Informationen in eine Mac-Typnummer. |
| [Getnpppatternfilterfromblob](getnpppatternfilterfromblob.md) | Ruft den Muster Übereinstimmungs Filter aus einem angegebenen BLOB ab.                                                                            |
| [Getnpptriggerfromblob](getnpptriggerfromblob.md)             | Ruft den Trigger eines angegebenen BLOB ab.                                                                                           |
| [Getstringfromblob](getstringfromblob.md)                     | Ruft eine einzelne Zeichenfolge von einer bestimmten Position in einem angegebenen BLOB ab.                                                          |
| [Getstringsfromblob](getstringsfromblob.md)                   | Ruft alle Zeichen folgen innerhalb der angegebenen Begrenzungen von einem angegebenen BLOB ab.                                                          |
| [Isremotenpp](isremotenpp.md)                                 | Gibt an, ob das angegebene BLOB eine Remote-NPP angibt.                                                                         |
| [Mergeblob](mergeblob.md)                                     | Führt die Informationen in Quell-und zielblobs zusammen und überschreibt allgemeine Einträge mit Daten aus dem Quell-BLOB.                  |
| [Regkreateblobkey](regcreateblobkey.md)                       | Speichert ein BLOB mit dem angegebenen Registrierungsschlüssel.                                                                                         |
| [Regopenblobkey](regopenblobkey.md)                           | Ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.                                                                               |
| [Removefromblob](removefromblob.md)                           | Entfernt Informationen aus einer beliebigen Ebene eines bestimmten BLOBs.                                                                              |
| [Selectnppblobfromtable](selectnppblobfromtable.md)           | Wählt ein NPP-BLOB aus einer Tabelle aus.                                                                                                |
| [Setboolinblob](setboolinblob.md)                             | Legt einen booleschen Wert an der angegebenen Position innerhalb eines BLOBs fest.                                                                        |
| [Setclassidinblob](setclassidinblob.md)                       | Legt den Wert der benannten Klassen Kennung für ein BLOB fest.                                                                                |
| [Setdwordinblob](setdwordinblob.md)                           | Legt den benannten **DWORD** -Wert für ein BLOB fest.                                                                                       |
| [Setmacaddressinblob](setmacaddressinblob.md)                 | Legt die benannte Mac-Adresse für ein BLOB fest.                                                                                           |
| [Setnetworkinfoinblob](setnetworkinfoinblob.md)               | Legt die Netzwerkinformationen für ein BLOB fest.                                                                                         |
| [Setnppaddressfilterinblob](setnppaddressfilterinblob.md)     | Legt den angegebenen Adress Filter im BLOB fest.                                                                                       |
| [Setnppeer Type esapfilter](setnppetypesapfilter.md)               | Legt den ETYPE/SAP-Filter in einem BLOB fest.                                                                                             |
| [Setnpppatternfilterinblob](setnpppatternfilterinblob.md)     | Legt den Muster Übereinstimmungs Filter für ein BLOB fest.                                                                                        |
| [Setnpptriggerinblob](setnpptriggerinblob.md)                 | Legt den Trigger in einem BLOB fest.                                                                                                      |
| [Setstringinblob](setstringinblob.md)                         | Legt die Zeichenfolge an einer angegebenen Position innerhalb eines BLOBs fest.                                                                               |
| ["Write-blobdefile"](writeblobtofile.md)                         | Schreibt ein BLOB in eine angegebene Datei.                                                                                                   |



 

 

 



