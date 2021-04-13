---
title: Test-und Produktions Schlüssel für einen Typ-1-Online Shop
description: Test-und Produktions Schlüssel für einen Typ-1-Online Shop
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player Online Stores, Testschlüssel
- Online Stores, Testschlüssel
- Typ 1 Online Stores, Testschlüssel
- Windows Media Player Online Stores, Produktions Schlüssel
- Online Stores, Produktions Schlüssel
- Typ 1 Online Stores, Produktions Schlüssel
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Testschlüssel
- Produktions Schlüssel
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388643"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>Test-und Produktions Schlüssel für einen Typ-1-Online Shop

Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei numerische Schlüssel: einen Testschlüssel und einen Produktions Schlüssel. Gleichzeitig müssen Sie Microsoft zwei URLs bereitstellen: eines, das auf Ihr Test serviceInfo-Dokument verweist, und eines, das auf Ihr Produktions-serviceInfo-Dokument verweist.

Während der Entwicklungs-und Testphase ist Ihr Online Store in Windows Media Player nur dann sichtbar, wenn sich Ihr Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet. Wenn sich Ihr Testschlüssel in der Registrierung befindet, ruft Windows Media Player das Test serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Bilder verweist, die zu Ihrem Test Speicher gehören. Wenn sich Ihr Produktions Schlüssel in der Registrierung befindet, ruft Windows Media Player das Produktions-serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Images verweist, die zu Ihrem Produktionsspeicher gehören.

Sie können Ihre Test-und Produktionsspeicher in beliebiger Weise verwenden, die Sie nützlich finden. In der Regel ist der Unterschied jedoch wie folgt:

-   Der Test Speicher ist der Ort, an dem Sie tägliche Änderungen an Ihrem Plug-in, Webseiten, Images und anderen Komponenten Ihres Dienstanbieter vornehmen.
-   Der Produktionsspeicher ist der Ort, an dem Sie eine stabile Version Ihres dienplatzes aufbewahren, die Ihr Plug-in, Webseiten, Bilder und andere Komponenten umfasst.

Bevor der Online Shop in Windows Media Player veröffentlicht werden kann, muss Microsoft überprüfen, ob der Dienst ordnungsgemäß ausgeführt wird. Während der Überprüfungsphase verwendet Microsoft ihren Produktions Schlüssel. Microsoft verwendet den Testschlüssel während der Überprüfungsphase nicht.

Wenn Ihr Onlinespeicher für die Produktion den Überprüfungsprozess erfolgreich abgeschlossen hat, veröffentlicht Microsoft ihren Store. Dies bedeutet, dass Ihr Produktionsspeicher in Windows Media Player für alle Benutzer angezeigt wird, nicht nur für diejenigen, die ihren Produktions Schlüssel in der Registrierung besitzen. Nach der Veröffentlichung des Stores werden die Test-und Produktions Schlüssel nicht mehr benötigt.

> [!Note]  
> Benutzer sind möglicherweise in der Lage, den Test-oder Produktions Schlüssel für Ihren Online Shop zu erraten und ihren Store während der Entwicklung anzuzeigen. Sie sollten sorgfältig vorgehen, wenn Sie die Features verfügbar machen möchten, die Sie geheim halten möchten, bis zum öffentlichen Release.

 

Ausführliche Informationen dazu, wo Sie Ihre Produktions-und Testschlüssel in der Registrierung des Benutzers platzieren, finden Sie unter [Registrierungsschlüssel und-Einträge für den Online Store des Typs 1](registry-keys-and-entries-for-a-type-1-online-store.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> </dl>

 

 




