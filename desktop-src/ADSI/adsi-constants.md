---
title: ADSI-Konstanten
description: Die folgende Tabelle enthält Konstanten, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023918"
---
# <a name="adsi-constants"></a>ADSI-Konstanten

Die folgende Tabelle enthält Konstanten, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.



| ADSI-Konstante                      | Wert                                   | BESCHREIBUNG                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ EXT \_ INITCREDENTIALS**      | 1                                       | Ein Steuerungscode, der angibt, dass die für die [**IADsExtension::Operate-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) bereitgestellten benutzerdefinierten Daten Benutzeranmeldeinformationen enthalten.                                                     |
| **ADS \_ EXT \_ INITIALIZE \_ COMPLETE** | 2                                       | Ein Steuerungscode, der mit [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) verwendet wird, um anzugeben, dass Erweiterungen je nach den vom übergeordneten Objekt unterstützten Funktionen jede erforderliche Initialisierung ausführen können. |
| **ADS \_ EXT \_ MAXEXTDISPID**         | 16777215                                | Die höchste DISPID, die ein Erweiterungsobjekt für seine Methoden und Eigenschaften verwenden kann.                                                                                                                                   |
| **ADS \_ EXT \_ MINEXTDISPID**         | 1                                       | Die niedrigste DISPID, die ein Erweiterungsobjekt für seine Methoden und Eigenschaften verwenden kann.                                                                                                                                    |
| **\_ADS-VLV-ANTWORT \_**             | L"fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Wird mit der [**IDirectorySearch::GetColumn-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) verwendet, um VLV-Suchmetadaten abzurufen. Weitere Informationen finden Sie unter [How to Search Using VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Wird für die Arbeit mit dem OLE DB verwendet.                                                                                                                                                                           |



 

 

 




