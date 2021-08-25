---
description: Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarieren und TAPI dann darüber informieren, welche Ressourcen sie verwendet und wie sie sie verwendet.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Ressourcenbestand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773420"
---
# <a name="resource-inventory"></a>Ressourcenbestand

Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarieren und TAPI dann darüber informieren, welche Ressourcen sie verwendet und wie sie sie verwendet. Weitere [Informationen zu den](device-control.md) Ressourcen- und Funktionentypen, auf die eine Anwendung zugreifen kann, finden Sie unter Gerätesteuerung.

**TAPI 2.x:** Anwendungen erhalten die Anzahl der verfügbaren Zeilen, [**wenn lineInitializeEx zurückgegeben**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) wird. Sie können dann [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für jede Zeile, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) für jede Adresse und [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) für jede verwendete Zeile ausführen.

**TAPI 3.x:** Anwendungen verwenden [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) oder [**ITTAPI::get \_ Addresses,**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) um die verfügbaren Adressen zu finden. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) und [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) stellen Informationen zu kommunikationstypen zur Verfügung, die für jede Adresse möglich sind. Wenn [**itterminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) vom Dienstanbieter implementiert wird, erhält eine Anwendung Zugriff auf zusätzliche Informationen und Steuerelemente.

 

 
