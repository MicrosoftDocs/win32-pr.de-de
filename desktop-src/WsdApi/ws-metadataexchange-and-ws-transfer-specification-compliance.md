---
description: Vor August 2006 WS-MetadataExchange eine eigene Get Metadata Exchange-Methode definiert, die von Devices Profile for Web Services (DPWS) verwendet wurde.
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: WS-MetadataExchange- und WS-Transfer Spezifikationskonformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793970"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>WS-MetadataExchange- und WS-Transfer Spezifikationskonformität

Vor August 2006 definierte [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) eine eigene [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Methode, die von [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) verwendet wurde. Die WS-MetadataExchange-Spezifikation Version 1.1 hat diese Methode durch die get-Methode ersetzt, die in der WS-Transfer-Spezifikation definiert ist.

Im aktuellen Modell stellt WS-Transfer die [Get-Methode](get--metadata-exchange--http-request-and-message.md) bereit und verweist nicht auf den Typ des Textkörpers. WS-MetadataExchange beschreibt das Format des Textkörpers und einen Mechanismus zum Packen mehrerer Metadaten in einer einzelnen Antwort, und DPWS beschreibt bestimmte Metadatenteile, die ein Dienst in eine Metadatenantwort einschließen sollte.

WSDAPI unterstützt die WS-Transfer-Spezifikation nicht vollständig. Da nur die [Get-Methode](get--metadata-exchange--http-request-and-message.md) für Geräte erforderlich ist, wurden keine anderen Teile von WS-Transfer implementiert. Darüber hinaus implementiert WSDAPI nicht die in WS-MetadataExchange beschriebene optionale GetMetadata-Methode.

 

 



