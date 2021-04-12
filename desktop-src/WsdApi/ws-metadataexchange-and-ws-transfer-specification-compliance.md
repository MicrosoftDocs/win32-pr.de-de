---
description: Vor August 2006 haben WS-MetadataExchange eine eigene Get Metadata Exchange-Methode definiert, die von Geräte Profilen für Webdienste (DPWS) verwendet wurde.
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Konformität von WS-MetadataExchange und WS-Transfer Spezifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130956"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Konformität von WS-MetadataExchange und WS-Transfer Spezifikation

Vor August 2006 hat [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) seine eigene [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Methode definiert, die von [Geräte Profilen für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) verwendet wurde. Die WS-MetadataExchange Specification Version 1,1 hat diese Methode durch die in der WS-Transfer Spezifikation definierte Get-Methode ersetzt.

Im aktuellen Modell stellt WS-Transfer die [Get](get--metadata-exchange--http-request-and-message.md) -Methode bereit und macht keinen Verweis auf den Typ des Texts. In WS-MetadataExchange wird das Format des Texts und ein Mechanismus zum Verpacken mehrerer Metadatenelemente in einer einzelnen Antwort beschrieben. Außerdem werden in DPWS bestimmte Metadatenelemente beschrieben, die ein Dienst in eine metadatenantwort einschließen sollte.

WSDAPI unterstützt die WS-Transfer Spezifikation nicht vollständig. Da nur die [Get](get--metadata-exchange--http-request-and-message.md) -Methode für Geräte erforderlich ist, sind keine anderen Teile der WS-Transfer implementiert. Außerdem implementiert WSDAPI nicht die optionale GetMetadata-Methode, die in WS-MetadataExchange beschrieben wird.

 

 



