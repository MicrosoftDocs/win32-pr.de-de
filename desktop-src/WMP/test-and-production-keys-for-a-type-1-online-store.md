---
title: Test- und Produktionsschlüssel für eine Online-Store
description: Test- und Produktionsschlüssel für eine Online-Store
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player,Testschlüssel
- Onlineshops,Testschlüssel
- Geben Sie 1 Onlineshops,Testschlüssel ein.
- Windows Media Player Onlineshops,Produktionsschlüssel
- Onlineshops,Produktionsschlüssel
- 'Typ 1: Onlineshops,Produktionsschlüssel'
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 1 Onlineshops,ServiceInfo-Dokument
- Testschlüssel
- Produktionsschlüssel
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00fcd1af52f7400b7f20a1eb3115bfc38d8b997bfbc85c5d6e36f08fcf59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118530"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>Test- und Produktionsschlüssel für eine Online-Store

Wenn Sie mit der Entwicklung Ihres Onlineshops beginnen, stellt Microsoft zwei numerische Schlüssel zur Verfügung: einen Testschlüssel und einen Produktionsschlüssel. Gleichzeitig müssen Sie Microsoft zwei URLs bereitstellen: eine, die auf Ihr ServiceInfo-Testdokument verweist, und eine, die auf Ihr ServiceInfo-Produktionsdokument verweist.

Während der Entwicklungs- und Testphase ist Ihr Onlineshop in Windows Media Player nur sichtbar, wenn sich Ihr Testschlüssel oder Ihr Produktionsschlüssel in der Registrierung auf dem Computer des Benutzers befindet. Wenn sich Ihr Testschlüssel in der Registrierung befindet, ruft Windows Media Player Ihr ServiceInfo-Testdokument ab, das auf das Plug-In, webseiten und Bilder verweist, die zu Ihrem Testspeicher gehören. Wenn sich Ihr Produktionsschlüssel in der Registrierung befindet, ruft Windows Media Player Ihr ServiceInfo-Produktionsdokument ab, das auf das Plug-In, webseiten und Images verweist, die zu Ihrem Produktionsspeicher gehören.

Sie können Ihre Test- und Produktionsspeicher auf jede Weise verwenden, die Sie für nützlich finden. In der Regel lautet der Unterschied jedoch wie folgt:

-   In Ihrem Testspeicher nehmen Sie täglich Änderungen an Ihrem Plug-In, an Webseiten, Bildern und anderen Komponenten Ihres Diensts vor.
-   Ihr Produktionsspeicher ist der Ort, an dem Sie eine stabile Version Ihres Diensts behalten, die Ihr Plug-In, Webseiten, Bilder und andere Komponenten umfasst.

Bevor Ihr Onlineshop in der Windows Media Player veröffentlicht werden kann, muss Microsoft überprüfen, ob Ihr Dienst ordnungsgemäß ausgeführt wird. Während der Überprüfungsphase verwendet Microsoft Ihren Produktionsschlüssel. Microsoft verwendet Ihren Testschlüssel während der Überprüfungsphase nicht.

Wenn ihr Produktions-Onlineshop den Überprüfungsprozess erfolgreich abgeschlossen hat, veröffentlicht Microsoft Ihren Store. Das bedeutet, dass Ihr Produktionsspeicher in Windows Media Player für alle Benutzer angezeigt wird, nicht nur für dieJenigen, die ihren Produktionsschlüssel in der Registrierung haben. Nachdem Ihr Speicher veröffentlicht wurde, werden die Test- und Produktionsschlüssel nicht mehr benötigt.

> [!Note]  
> Benutzer können möglicherweise den Test- oder Produktionsschlüssel für Ihren Onlineshop erraten und Ihren Store während der Entwicklung anzeigen. Sie sollten sorgfältig darauf achten, Features verfügbar zu machen, die Sie bis zur Veröffentlichung geheim halten möchten.

 

Ausführliche Informationen dazu, wo Ihre Produktions- und Testschlüssel in der Registrierung des Benutzers gespeichert werden, finden Sie unter Registrierungsschlüssel und Einträge für einen Onlineschlüssel vom Typ [1 Store](registry-keys-and-entries-for-a-type-1-online-store.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




