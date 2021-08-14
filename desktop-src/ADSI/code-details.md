---
title: Codedetails
description: In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispielanbieterkomponente aufgelistet. Alle Quellcodeverweise in diesem Dokument können geändert werden und sind im Beispielcodeverzeichnis verfügbar, das im ADSI SDK enthalten ist.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Codedetails ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f03e7c7ed7d61d56f338a8bb44d51b1890d4bd24cd7dc1e6050f1900f6ff61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692286"
---
# <a name="code-details"></a>Codedetails

In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispielanbieterkomponente aufgelistet. Alle Quellcodeverweise in diesem Dokument können geändert werden und sind im Beispielcodeverzeichnis verfügbar, das im ADSI SDK enthalten ist.

> [!Note]  
> Die [**IADs-Methoden**](/windows/desktop/api/Iads/nn-iads-iads) **GetEx** und **PutEx** sind in der ADSI-Beispielanbieterkomponente nicht implementiert. Das heißt, Code, der Active Directory-Objekte implementiert, die von **IADs** erben, verfügt nicht über **die Methoden GetEx** und **PutEx.** Dazu gehören das Schemaklassenobjekt, das [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)unterstützt, das Eigenschaftenobjekt, das [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)unterstützt, das generische Active Directory-Objekt, das **IADs** unterstützt, und alle Containerobjekte, die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)unterstützen. Darüber hinaus sind Syntaxobjekte in der Beispielanbieterkomponente nicht vorhanden. Die ADSI-Architektur erfordert jedoch, dass die Syntaxobjekte in das Schemacontainerobjekt eingeschlossen werden, ebenso wie die Schemaklasse und eigenschaftenobjekte.

 

Die folgende Tabelle enthält Quellcodedateien, die im Beispielverzeichnis des Anbieters im Active Directory Service Interfaces SDK enthalten sind.



| Quellcodedatei                 | Beschreibung                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj.cpp](cclsobj-cpp.md)   | Schemaklassenobjektroutinen.                                                                                                                                     |
| [cdispmgr.cpp](cdispmgr-cpp.md) | Dispatch Manager-Implementierung.                                                                                                                                  |
| [cenumns.cpp](cenumns-cpp.md)   | Namespaceenumerationsroutinen.                                                                                                                                   |
| [cenumsch.cpp](cenumsch-cpp.md) | Schemaenumerationsroutinen.                                                                                                                                      |
| [cenumobj.cpp](cenumobj-cpp.md) | Generische Objektenumerationsroutinen.                                                                                                                              |
| [cenumvar.cpp](cenumvar-cpp.md) | Basisimplementierungen für von xxxEnumVariant abgeleitete Klassen.                                                                                                           |
| [cgenobj.cpp](cgenobj-cpp.md)   | Generische Objektroutinen.                                                                                                                                          |
| [cnamcf.cpp](cnamcf-cpp.md)     | Namespaceklassenfactoryroutinen.                                                                                                                                 |
| [cnamesp.cpp](cnamesp-cpp.md)   | Namespaceobjektroutinen.                                                                                                                                        |
| [common.cpp](common-cpp.md)     | Code, der allen Anbieterobjekten gemeinsam ist.                                                                                                                              |
| [core.cpp](core-cpp.md)         | Implementierungen für Kerneigenschaften, die von allen Active Directory-Objekten gemeinsam genutzt werden.                                                                                     |
| [cprops.cpp](cprops-cpp.md)     | Eigenschaftencachefeatures.                                                                                                                                          |
| [cprov.cpp](cprov-cpp.md)       | Anbieterobjektroutinen der obersten Ebene.                                                                                                                               |
| [cprovcf.cpp](cprovcf-cpp.md)   | Factoryroutinen der Anbieterobjektklasse der obersten Ebene.                                                                                                                 |
| [cprpobj.cpp](cprpobj-cpp.md)   | Eigenschaftenobjektroutinen.                                                                                                                                         |
| [cschobj.cpp](cschobj-cpp.md)   | Schemaobjektroutinen.                                                                                                                                           |
| [getobj.cpp](getobj-cpp.md)     | GetObject-Funktion.                                                                                                                                                |
| [globals.cpp](globals-cpp.md)   | ADSI-Beispielanbieterkomponenten – globale Komponenten.                                                                                                                          |
| [guid.cpp](guid-cpp.md)         | Beispielanbieterkomponenten-CLSIDs und LIBIDs.                                                                                                                     |
| [libmain.cpp](libmain-cpp.md)   | Libmain für adssmp.dll.                                                                                                                                           |
| [memory.cpp](memory-cpp.md)     | Beispielroutinen für die Speicherverwaltung von Anbieterkomponenten.                                                                                                            |
| [pack.cpp](pack-cpp.md)         | Beispiel für das Packen/Entpacken von Daten in VTARTS durch Anbieterkomponenten.                                                                                                          |
| [parse.cpp](parse-cpp.md)       | Pfadparsierung, z. B. Anbieterkomponentennamespace.                                                                                                            |
| [property.cpp](property-cpp.md) | Abrufen und Legen Sie die Eigenschaften nach Namen ab.                                                                                                                                   |
| [object.cpp](object-cpp.md)     | Beispielcode für die Objekttypliste der Anbieterkomponente für die Filterung.                                                                                                   |
| [regdsapi.cpp](regdsapi-cpp.md) | Beispiel für Verzeichnisdienst-APIs der Anbieterkomponentenregistrierung.                                                                                                       |
| smpoper.cpp                      | Datenkonvertierungsroutinen.                                                                                                                                         |
| [stdfact.cpp](stdfact-cpp.md)   | IClassFactory-Standardimplementierungen. [](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)                                                                                                  |
| adssmp.inf                       | Beispielregistrierungsdaten des Verzeichnisdatenspeichers. Weitere Informationen finden Sie unter [Installieren der Beispielanbieterkomponente](installing-the-example-provider-component.md). |



 

 

 