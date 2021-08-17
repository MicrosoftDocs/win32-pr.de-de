---
description: Behandeln von COM+-Verwaltungsfehlern
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Behandeln von COM+-Verwaltungsfehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965276fff68edf45ae27423ee4ed707e4bb7f1476b0237dab270538e0fa0f1be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306708"
---
# <a name="handling-com-administration-errors"></a>Behandeln von COM+-Verwaltungsfehlern

Fehler, die bei Verwendung der COMAdmin-Objekte generiert werden, werden wie folgt auf zwei Arten gemeldet:

-   Verwenden von spezifischen Fehlercodes für die COMAdmin-Bibliothek.
-   Verwenden erweiterter Fehlerinformationen, die in einer speziellen [**ErrorInfo-Auflistung verfügbar**](errorinfo.md) sind.

## <a name="error-codes"></a>Fehlercodes

Sie behandeln Fehlercodes für die Verwaltung wie alle COM-Fehlermeldungen. In Microsoft Visual C++ werden diese Codes als **HRESULT-Werte** zurückgegeben. In Microsoft Visual Basic werden sie als Ausnahmen ausgelöst, die Sie abfangen können. Für C++-Programmierer werden die COM+-Verwaltungsfehlercodes in Winerror.h definiert. Für Visual Basic Programmierer sind sie über die Visual Basic IDE verfügbar.

## <a name="errorinfo-collection"></a>ErrorInfo-Auflistung

Wenn ein Fehler auftritt, der durch eine Art von Fehlercode signalisiert wird, sind je nach Art des Fehlers möglicherweise ausführlichere Informationen verfügbar. Die COMAdmin-Objekte stellen erweiterte Informationen in Situationen zur Verfügung, in denen die genaue Ursache des Fehlers ohne detaillierten Bericht schwierig zu ermitteln ist, z. B. bei mehreren Lese- und Schreibvorgängen.

Wenn Sie beispielsweise Methoden wie [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für ein [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) verwenden, können Sie Daten für jedes Element in der Auflistung lesen oder schreiben. Komplizierte Fehler können auftreten, und es kann schwierig sein, sie basierend auf einem einzelnen numerischen Fehlercode zu diagnostizieren. Aus diesem Grund erstellt die COMAdmin-Bibliothek erweiterte Fehlerinformationen über eine spezielle Sammlung.

Wenn erweiterte Fehlerinformationen verfügbar sind, werden sie in der [**ErrorInfo-Auflistung**](errorinfo.md) platziert, die mit der ursprünglichen Auflistung verknüpft ist, bei der der Fehler aufgetreten ist. Rufen Sie zum Abrufen des Fehlerberichts die **ErrorInfo-Auflistung** ab, die sich auf die ursprüngliche Sammlung bezieht, und untersuchen Sie die elemente, die sie enthält. Sie können die **ErrorInfo-Sammlung** abrufen, indem Sie [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) für [**COMAdminCatalogCollection**](comadmincatalogcollection.md)verwenden und den zweiten Parameter leer lassen, in dem Sie normalerweise die Key-Eigenschaft eines übergeordneten Elements angeben würden.

Wenn sie einen Fehler erhalten, müssen Sie sofort die [**ErrorInfo-Auflistung**](errorinfo.md) für die fehlgeschlagene Sammlung erhalten und auffüllen, ohne andere Vorgänge für diese Sammlung ausführen zu müssen. Andernfalls wird **die ErrorInfo-Auflistung** zurückgesetzt und gibt diesen Fehler nicht an.

Die Elemente in der [**ErrorInfo-Auflistung**](errorinfo.md) machen die speziellen Fehlerberichterstattungseigenschaften MajorRef und MinorRef verfügbar, die die spezielle Ursache des Fehlers detailliert beschreiben. Weitere Informationen finden Sie unter **ErrorInfo**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



