---
description: Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarisieren und TAPI darüber benachrichtigen, welche Ressourcen von der Anwendung verwendet werden und wie Sie verwendet werden.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Ressourcen Inventur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363460"
---
# <a name="resource-inventory"></a>Ressourcen Inventur

Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarisieren und TAPI darüber benachrichtigen, welche Ressourcen von der Anwendung verwendet werden und wie Sie verwendet werden. Weitere Informationen zu den Arten von Ressourcen und Funktionen, auf die eine Anwendung zugreifen kann, finden Sie unter [Gerätesteuerung](device-control.md) .

**TAPI 2. x:** Anwendungen erhalten die Anzahl der verfügbaren Zeilen, wenn [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) zurückgibt. Anschließend können Sie [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für jede Zeile, [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) für jede Adresse und [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) für jede zu verwendende Zeile ausführen.

**TAPI 3. x:** Anwendungen verwenden die Adressen [**ittapi:: enumerateadressen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) oder [**ittapi: \_ : Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) , um die verfügbaren Adressen zu ermitteln. [**Itmediasupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) und [**itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) stellen Informationen zu Kommunikationstypen bereit, die für jede Adresse möglich sind. Durch die Implementierung durch den Dienstanbieter erhält [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) eine Anwendung Zugriff auf zusätzliche Informationen und Steuerelemente.

 

 
