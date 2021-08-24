---
description: Netzwerkmonitor enthält die folgenden BLOB-Funktionen.
ms.assetid: 90514067-59e9-4bd9-8612-2263bd414574
title: BLOB-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654fb7e7c6879a6df0f3b4aad4d29007a9405186631bd4d9c4dc1a24e606eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144363"
---
# <a name="blob-functions"></a>BLOB-Funktionen

Netzwerkmonitor enthält die folgenden BLOB-Funktionen.



| Funktion                                                       | Beschreibung                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [CreateBlob](createblob.md)                                   | Erstellt ein leeres BLOB.                                                                                                           |
| [CreateNPPInterface](createnppinterface.md)                   | Erstellt eine NPP-Schnittstelle mit einem angegebenen BLOB.                                                                                      |
| [DestroyBlob](destroyblob.md)                                 | Gibt den vollständigen Speicher frei, der einem bestimmten BLOB zugeordnet ist.                                                                                   |
| [DuplicateBlob](duplicateblob.md)                             | Kopiert ein bestimmtes BLOB.                                                                                                             |
| [GetBoolFromBlob](getboolfromblob.md)                         | Ruft den benannten booleschen Wert aus einem angegebenen BLOB ab.                                                                             |
| [GetClassIDFromBlob](getclassidfromblob.md)                   | Ruft den benannten Klassenbezeichnerwert aus einem angegebenen BLOB ab.                                                                    |
| [GetDwordFromBlob](getdwordfromblob.md)                       | Ruft den benannten **DWORD-Wert** aus einem angegebenen BLOB ab.                                                                           |
| [GetMacAddressFromBlob](getmacaddressfromblob.md)             | Ruft die benannte MAC-Adresse aus einem angegebenen BLOB ab.                                                                               |
| [GetNetworkInfoFromBlob](getnetworkinfofromblob.md)           | Ruft Netzwerkinformationen aus einem angegebenen BLOB ab.                                                                                 |
| [GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md) | Ruft Adressfilterinformationen aus einem angegebenen BLOB ab.                                                                          |
| [GetNPPBlobFromUI](getnppblobfromui.md)                       | Zeigt das **Dialogfeld Netzwerk auswählen** an und gibt das NPP-BLOB der ausgewählten NIC zurück.                                       |
| [GetNPPBlobTable](getnppblobtable.md)                         | Ruft eine Tabelle mit BLOBs ab.                                                                                                      |
| [GetNPPEtypeSapFilter](getnppetypesapfilter.md)               | Ruft den Etype/Sap-Filter aus einem angegebenen BLOB ab.                                                                                |
| [GetNPPMacTypeAsNumber](getnppmactypeasnumber.md)             | Ruft den MAC-Typ aus der **Kategorie NetworkInfo** des NPP-Abschnitts ab und konvertiert die Informationen in eine MAC-Typnummer. |
| [GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md) | Ruft den Muster match-Filter aus einem angegebenen BLOB ab.                                                                            |
| [GetNPPTriggerFromBlob](getnpptriggerfromblob.md)             | Ruft den Trigger eines angegebenen BLOB ab.                                                                                           |
| [GetStringFromBlob](getstringfromblob.md)                     | Ruft eine einzelne Zeichenfolge von einem bestimmten Speicherort in einem bestimmten BLOB ab.                                                          |
| [GetStringsFromBlob](getstringsfromblob.md)                   | Ruft alle Zeichenfolgen innerhalb der angegebenen Grenzen aus einem angegebenen BLOB ab.                                                          |
| [IsRemoteNPP](isremotenpp.md)                                 | Gibt an, ob das gegebene BLOB ein Remote-NPP angibt.                                                                         |
| [MergeBlob](mergeblob.md)                                     | Führt die Informationen in Quell- und Ziel-BLOBs zusammen und überschreibt allgemeine Einträge mit Daten aus dem Quellblob.                  |
| [RegCreateBlobKey](regcreateblobkey.md)                       | Speichert ein BLOB unter dem angegebenen Registrierungsschlüssel.                                                                                         |
| [RegOpenBlobKey](regopenblobkey.md)                           | Ruft ein BLOB ab, das unter dem angegebenen Registrierungsschlüssel gespeichert ist.                                                                               |
| [RemoveFromBlob](removefromblob.md)                           | Entfernt Informationen aus jeder Ebene eines bestimmten BLOB.                                                                              |
| [SelectNPPBlobFromTable](selectnppblobfromtable.md)           | Wählt ein NPP-BLOB aus einer Tabelle aus.                                                                                                |
| [SetBoolInBlob](setboolinblob.md)                             | Legt einen booleschen Wert an der angegebenen Position in einem BLOB fest.                                                                        |
| [SetClassIDInBlob](setclassidinblob.md)                       | Legt den benannten Klassenbezeichnerwert für ein BLOB fest.                                                                                |
| [SetDwordInBlob](setdwordinblob.md)                           | Legt den benannten **DWORD-Wert** für ein BLOB fest.                                                                                       |
| [SetMacAddressInBlob](setmacaddressinblob.md)                 | Legt die benannte MAC-Adresse für ein BLOB fest.                                                                                           |
| [SetNetworkInfoInBlob](setnetworkinfoinblob.md)               | Legt die Netzwerkinformationen für ein BLOB fest.                                                                                         |
| [SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)     | Legt den angegebenen Adressfilter im BLOB fest.                                                                                       |
| [SetNPPEtypeSapFilter](setnppetypesapfilter.md)               | Legt den Etype/Sap-Filter in einem BLOB fest.                                                                                             |
| [SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)     | Legt den Muster match-Filter für ein BLOB fest.                                                                                        |
| [SetNPPTriggerInBlob](setnpptriggerinblob.md)                 | Legt den Trigger in einem BLOB fest.                                                                                                      |
| [SetStringInBlob](setstringinblob.md)                         | Legt die Zeichenfolge an einer bestimmten Position in einem BLOB fest.                                                                               |
| [WriteBlobToFile](writeblobtofile.md)                         | Schreibt ein BLOB in eine bestimmte Datei.                                                                                                   |



 

 

 



