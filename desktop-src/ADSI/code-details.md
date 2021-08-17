---
title: Codedetails
description: In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispielanbieterkomponente aufgeführt. Alle Quellcodeverweise in diesem Dokument können geändert werden und sind im Beispielcodeverzeichnis verfügbar, das im ADSI SDK enthalten ist.
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

In diesem Abschnitt wird der Quellcode für die Implementierung der ADSI-Beispielanbieterkomponente aufgeführt. Alle Quellcodeverweise in diesem Dokument können geändert werden und sind im Beispielcodeverzeichnis verfügbar, das im ADSI SDK enthalten ist.

> [!Note]  
> Die [**IADs-Methoden**](/windows/desktop/api/Iads/nn-iads-iads) **GetEx** und **PutEx** sind in der ADSI-Beispielanbieterkomponente nicht implementiert. Das bedeutet, dass Code, der Active Directory-Objekte implementiert, die von **IADs** erben, keine **GetEx-** und **PutEx-Methoden** hat. Dazu gehören das Schemaklassenobjekt, das [**IADsClass unterstützt,**](/windows/desktop/api/Iads/nn-iads-iadsclass)das Eigenschaftenobjekt, das [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)unterstützt, das generische Active Directory-Objekt, das **IADs** unterstützt, und jedes Containerobjekt, das [**IADsContainer unterstützt.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Darüber hinaus sind Syntaxobjekte in der Beispielanbieterkomponente nicht vorhanden. Die ADSI-Architektur erfordert jedoch, dass die Syntaxobjekte im Schemacontainerobjekt enthalten sind, genau wie die Schemaklasse und die Eigenschaftenobjekte.

 

In der folgenden Tabelle sind Quellcodedateien aufgeführt, die im Beispielverzeichnis des Anbieters im Active Directory Service Interfaces SDK enthalten sind.



| Quellcodedatei                 | Beschreibung                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj.cpp](cclsobj-cpp.md)   | Schemaklassenobjektroutinen.                                                                                                                                     |
| [cdispmgr.cpp](cdispmgr-cpp.md) | Dispatch Manager-Implementierung.                                                                                                                                  |
| [cenumns.cpp](cenumns-cpp.md)   | Namespaceenumerationsroutinen.                                                                                                                                   |
| [cenumsch.cpp](cenumsch-cpp.md) | Schemaenumerationsroutinen.                                                                                                                                      |
| [cenumobj.cpp](cenumobj-cpp.md) | Generische Objektenumerationsroutinen.                                                                                                                              |
| [cenumvar.cpp](cenumvar-cpp.md) | Basisimplementierung für abgeleitete xxxEnumVariant-Klassen.                                                                                                           |
| [cgenobj.cpp](cgenobj-cpp.md)   | Generische Objektroutinen.                                                                                                                                          |
| [cnamcf.cpp](cnamcf-cpp.md)     | Namespaceklassen-Factoryroutinen.                                                                                                                                 |
| [cnamesp.cpp](cnamesp-cpp.md)   | Namespaceobjektroutinen.                                                                                                                                        |
| [common.cpp](common-cpp.md)     | Code, der allen Anbieterobjekten gemeinsam ist.                                                                                                                              |
| [core.cpp](core-cpp.md)         | Implementierungen für "Core"-Eigenschaften, die von allen Active Directory-Objekten gemeinsam genutzt werden.                                                                                     |
| [cprops.cpp](cprops-cpp.md)     | Eigenschaftencachefeatures.                                                                                                                                          |
| [cprov.cpp](cprov-cpp.md)       | Anbieterobjektroutinen der obersten Ebene.                                                                                                                               |
| [cprovcf.cpp](cprovcf-cpp.md)   | Factoryroutinen der Anbieterobjektklasse der obersten Ebene.                                                                                                                 |
| [cprpobj.cpp](cprpobj-cpp.md)   | Eigenschaftenobjektroutinen.                                                                                                                                         |
| [cschobj.cpp](cschobj-cpp.md)   | Schemaobjektroutinen.                                                                                                                                           |
| [getobj.cpp](getobj-cpp.md)     | GetObject-Feature.                                                                                                                                                |
| [globals.cpp](globals-cpp.md)   | Globale AdsI-Beispielanbieterkomponenten.                                                                                                                          |
| [guid.cpp](guid-cpp.md)         | Beispielanbieterkomponenten-CLSIDs und LIBIDs.                                                                                                                     |
| [libmain.cpp](libmain-cpp.md)   | Libmain für adssmp.dll.                                                                                                                                           |
| [memory.cpp](memory-cpp.md)     | Beispielroutinen für die Speicherverwaltung von Anbieterkomponenten.                                                                                                            |
| [pack.cpp](pack-cpp.md)         | Beispiel für das Packen/Entpacken von Daten von Anbieterkomponenten in VARIANTs.                                                                                                          |
| [parse.cpp](parse-cpp.md)       | Pfadparsing für den Namespace der Anbieterkomponente.                                                                                                            |
| [property.cpp](property-cpp.md) | Get and Put properties by name (Eigenschaften nach Namen erhalten und festlegen).                                                                                                                                   |
| [object.cpp](object-cpp.md)     | Beispielcode für die Liste der Anbieterkomponentenobjekttypen für die Filterung.                                                                                                   |
| [regdsapi.cpp](regdsapi-cpp.md) | Beispielanbieterkomponenten-Registrierungsverzeichnisdienst-APIs.                                                                                                       |
| smpoper.cpp                      | Datenkonvertierungsroutinen.                                                                                                                                         |
| [stdfact.cpp](stdfact-cpp.md)   | [**IClassFactory-Standardimplementierung.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)                                                                                                  |
| adssmp.inf                       | Beispiel für Verzeichnisdatenspeicher-Registrierungsdaten. Weitere Informationen finden Sie unter [Installieren der Beispielanbieterkomponente.](installing-the-example-provider-component.md) |



 

 

 