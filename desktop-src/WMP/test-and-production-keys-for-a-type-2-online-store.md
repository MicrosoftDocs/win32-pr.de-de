---
title: Test-und Produktions Schlüssel für einen Typ 2-Online Shop
description: Test-und Produktions Schlüssel für einen Typ 2-Online Shop
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player Online Stores, Testschlüssel
- Online Stores, Testschlüssel
- Typ 2 Online Stores, Testschlüssel
- Windows Media Player Online Stores, Produktions Schlüssel
- Online Stores, Produktions Schlüssel
- Typ 2 Online Stores, Produktions Schlüssel
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Testschlüssel
- Produktions Schlüssel
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947989"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Test-und Produktions Schlüssel für einen Typ 2-Online Shop

Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei numerische Schlüssel: einen Testschlüssel und einen Produktions Schlüssel. Gleichzeitig müssen Sie Microsoft zwei URLs bereitstellen: eines, das auf Ihr Test serviceInfo-Dokument verweist, und eines, das auf Ihr Produktions-serviceInfo-Dokument verweist.

Während der Entwicklungs-und Testphase ist Ihr Online Store in Windows Media Player nur dann sichtbar, wenn sich Ihr Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet. Wenn sich Ihr Testschlüssel in der Registrierung befindet, ruft Windows Media Player das Test serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Bilder verweist, die zu Ihrem Test Speicher gehören. Wenn sich Ihr Produktions Schlüssel in der Registrierung befindet, ruft Windows Media Player das Produktions-serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Images verweist, die zu Ihrem Produktionsspeicher gehören.

Sie können Ihre Test-und Produktionsspeicher in beliebiger Weise verwenden, die Sie nützlich finden. In der Regel ist der Unterschied jedoch wie folgt:

-   Der Test Speicher ist der Ort, an dem Sie tägliche Änderungen an Ihrem Plug-in, Webseiten, Images und anderen Komponenten Ihres Dienstanbieter vornehmen.
-   Der Produktionsspeicher ist der Ort, an dem Sie eine stabile Version Ihres dienplatzes aufbewahren, die Ihr Plug-in, Webseiten, Bilder und andere Komponenten umfasst.

Bevor der Online Shop in Windows Media Player veröffentlicht werden kann, muss Microsoft überprüfen, ob der Dienst ordnungsgemäß ausgeführt wird. Während der Überprüfungsphase verwendet Microsoft ihren Produktions Schlüssel. Microsoft verwendet den Testschlüssel während der Überprüfungsphase nicht.

Wenn Ihr Onlinespeicher für die Produktion den Überprüfungsprozess erfolgreich abgeschlossen hat, veröffentlicht Microsoft ihren Store. Dies bedeutet, dass Ihr Produktionsspeicher in Windows Media Player für alle Benutzer angezeigt wird, nicht nur für diejenigen, die ihren Produktions Schlüssel in der Registrierung besitzen. Nach der Veröffentlichung des Stores werden die Test-und Produktions Schlüssel nicht mehr benötigt.

> [!Note]  
> Benutzer sind möglicherweise in der Lage, den Test-oder Produktions Schlüssel für Ihren Online Shop zu erraten und ihren Store während der Entwicklung anzuzeigen. Sie sollten sorgfältig vorgehen, wenn Sie die Features verfügbar machen möchten, die Sie geheim halten möchten, bis zum öffentlichen Release.

 

Ausführliche Informationen dazu, wo Sie Produktions-und Testschlüssel in der Registrierung des Benutzers platzieren, finden Sie unter [Registrierungsschlüssel und-Einträge für den Online Store vom Typ 2](registry-keys-and-entries-for-a-type-2-online-store.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 2 Online Stores**](about-type-2-online-stores.md)
</dt> <dt>

[**Type 2 Online Store-Beispiele**](type-2-online-store-samples.md)
</dt> </dl>

 

 




