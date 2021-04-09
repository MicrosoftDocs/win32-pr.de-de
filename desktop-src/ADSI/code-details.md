---
title: Code Details
description: In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispiel Anbieter Komponente aufgeführt. Alle Quell Code Verweise in diesem Dokument unterliegen Änderungen und sind im Beispielcode Verzeichnis verfügbar, das im ADSI SDK enthalten ist.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Code Details ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d959357f2cdd094b26cde4f649c3286389b8415
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039598"
---
# <a name="code-details"></a>Code Details

In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispiel Anbieter Komponente aufgeführt. Alle Quell Code Verweise in diesem Dokument unterliegen Änderungen und sind im Beispielcode Verzeichnis verfügbar, das im ADSI SDK enthalten ist.

> [!Note]  
> Die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Methoden **Getex** und **PutEx** sind nicht in der ADSI-Beispiel Anbieter Komponente implementiert. Das heißt, Code, der Active Directory Objekte implementiert, die von **IADs** erben, verfügt nicht über **Getex** -und **PutEx** -Methoden. Dies schließt das Schema Klassenobjekt ein, das [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)unterstützt, das Eigenschafts Objekt, das [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)unterstützt, das generische Active Directory Objekt, das **IADs** unterstützt, und ein beliebiges Container Objekt, das [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)unterstützt. Außerdem sind Syntax Objekte nicht in der Beispiel Anbieter Komponente vorhanden. Die ADSI-Architektur erfordert jedoch, dass die Syntax Objekte im Schema Container Objekt enthalten sind, ebenso wie die Schema Klasse und die Eigenschafts Objekte.

 

In der folgenden Tabelle sind Quell Code Dateien aufgelistet, die im Beispiel Verzeichnis des Anbieters im Active Directory Dienst Schnittstellen-SDK enthalten sind.



| Quell Code Datei                 | BESCHREIBUNG                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj. cpp](cclsobj-cpp.md)   | Schema Klassen-Objekt Routinen.                                                                                                                                     |
| [cdispmgr. cpp](cdispmgr-cpp.md) | Dispatch-Manager-Implementierung.                                                                                                                                  |
| [cenum NS. cpp](cenumns-cpp.md)   | Namespace-enumerationsroutinen.                                                                                                                                   |
| [cenum Sch. cpp](cenumsch-cpp.md) | Schemenumerationsroutinen.                                                                                                                                      |
| [cenumubj. cpp](cenumobj-cpp.md) | Generische objektenumerationsroutinen.                                                                                                                              |
| [cenum var. cpp](cenumvar-cpp.md) | Basis Implementierung für von xxxenenumvariant abgeleitete Klassen.                                                                                                           |
| [cgenobj. cpp](cgenobj-cpp.md)   | Generische Objekt Routinen.                                                                                                                                          |
| [cnamcf. cpp](cnamcf-cpp.md)     | Namespace-Klassenfactory-Routinen.                                                                                                                                 |
| [cnamesp. cpp](cnamesp-cpp.md)   | Namespace-Objekt Routinen.                                                                                                                                        |
| [Common. cpp](common-cpp.md)     | Code, der allen Anbieter Objekten gemeinsam ist.                                                                                                                              |
| [Core. cpp](core-cpp.md)         | Implementierungen für "Core"-Eigenschaften, die von allen Active Directory Objekten gemeinsam genutzt werden.                                                                                     |
| [c-Eigenschaften. cpp](cprops-cpp.md)     | Eigenschaften Cache Features.                                                                                                                                          |
| [cprov. cpp](cprov-cpp.md)       | Anbieter Objekt Routinen der obersten Ebene.                                                                                                                               |
| [cprovcf. cpp](cprovcf-cpp.md)   | Klassen Routinen für Anbieter Objektklassen der obersten Ebene.                                                                                                                 |
| [cprpobj. cpp](cprpobj-cpp.md)   | Eigenschafts Objekt Routinen.                                                                                                                                         |
| [cschobj. cpp](cschobj-cpp.md)   | Schema Objekt Routinen.                                                                                                                                           |
| [getobj. cpp](getobj-cpp.md)     | GetObject-Feature.                                                                                                                                                |
| [Globals. cpp](globals-cpp.md)   | ADSI-Beispiel Anbieter Komponente Globals.                                                                                                                          |
| [GUID. cpp](guid-cpp.md)         | Beispiel Anbieter Komponenten-CLSIDs und ligebote.                                                                                                                     |
| [LibMain. cpp](libmain-cpp.md)   | LibMain für adssmp.dll.                                                                                                                                           |
| [Arbeitsspeicher. cpp](memory-cpp.md)     | Beispiel Routinen für die Speicherverwaltung von Anbieter Komponenten.                                                                                                            |
| [Paket. cpp](pack-cpp.md)         | Beispiel Anbieter Komponenten Paket/entpacken von Daten in Varianten.                                                                                                          |
| [analysieren. cpp](parse-cpp.md)       | Die Pfad--Verarbeitung für den Beispiel Anbieter Komponenten-Namespace.                                                                                                            |
| [Property. cpp](property-cpp.md) | Eigenschaften mit dem Namen "Get" und "Put".                                                                                                                                   |
| [Object. cpp](object-cpp.md)     | Beispielcode für den Objekttyp der Anbieter Komponente zum Filtern.                                                                                                   |
| [regdsapi. cpp](regdsapi-cpp.md) | Beispiel-APIs für den Registrierungs Verzeichnisdienst für Anbieter Komponenten.                                                                                                       |
| smpoper. cpp                      | Daten Konvertierungs Routinen.                                                                                                                                         |
| [stdfact. cpp](stdfact-cpp.md)   | Standard Implementierung von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .                                                                                                  |
| adssmp. inf                       | Beispiel Registrierungsdaten für den Verzeichnis Datenspeicher. Weitere Informationen finden Sie unter [Installieren der Beispiel Anbieter Komponente](installing-the-example-provider-component.md). |



 

 

 