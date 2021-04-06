---
title: ADSI-Konstanten
description: In der folgenden Tabelle sind die Konstanten aufgelistet, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.
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
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707487"
---
# <a name="adsi-constants"></a>ADSI-Konstanten

In der folgenden Tabelle sind die Konstanten aufgelistet, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.



| ADSI-Konstante                      | Wert                                   | BESCHREIBUNG                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ - \_ Anmelde Informationen**      | 1                                       | Ein Steuercode, der angibt, dass die benutzerdefinierten Daten, die für die [**iadsextension::**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Operation-Methode bereitgestellt werden, Benutzer Anmelde Informationen enthalten                                                     |
| **Werbung \_ zum \_ Initialisieren von anzeigen \_** | 2                                       | Ein Steuerelement Code, der mit [**iadsextension::**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Operation verwendet wird, um anzugeben, dass Erweiterungen jede erforderliche Initialisierung ausführen können, abhängig von den Funktionen, die vom übergeordneten Objekt unterstützt werden. |
| **ADS \_ Ext \_ maxextdispid**         | 16777215                                | Die höchste dispid, die ein Erweiterungs Objekt für seine Methoden und Eigenschaften verwenden kann.                                                                                                                                   |
| **ADS \_ Ext \_ minextdispid**         | 1                                       | Die niedrigste DISPID, die ein Erweiterungs Objekt für seine Methoden und Eigenschaften verwenden kann.                                                                                                                                    |
| **Anzeigen der \_ VLV- \_ Antwort**             | L "fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Wird mit der [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) -Methode zum Abrufen von VLV-Such Metadaten verwendet. Weitere Informationen finden Sie unter Vorgehens [Weise beim Suchen mit VLV](how-to-search-using-vlv.md).        |
| **dbpropflags \_ adsisearch**        | 0x0000c000                              | Wird verwendet, um mit dem OLE DB-Anbieter zu arbeiten.                                                                                                                                                                           |



 

 

 




