---
description: Behandeln von com+-Verwaltungsfehlern
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Behandeln von com+-Verwaltungsfehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346444"
---
# <a name="handling-com-administration-errors"></a>Behandeln von com+-Verwaltungsfehlern

Fehler, die bei der Verwendung der COMAdmin-Objekte generiert werden, werden auf zwei Arten wie folgt gemeldet:

-   Verwendung von für die COMAdmin-Bibliothek spezifischen Fehlercodes.
-   Verwendung erweiterter Fehlerinformationen, die in einer speziellen [**errorInfo**](errorinfo.md) -Sammlung verfügbar sind.

## <a name="error-codes"></a>Fehlercodes

Sie behandeln Verwaltungsfehler Codes wie jede beliebige com-Fehlermeldung. In Microsoft Visual C++ werden diese Codes als **HRESULT** -Werte zurückgegeben. In Microsoft Visual Basic werden Sie als Ausnahmen ausgelöst, die Sie erfassen können. Für C++-Programmierer sind die com+-Verwaltungsfehler Codes in WinError. h definiert. Für Visual Basic Programmierer sind Sie über die Visual Basic IDE verfügbar.

## <a name="errorinfo-collection"></a>ErrorInfo-Sammlung

Wenn ein Fehler auftritt, der durch eine Art von Fehlercode signalisiert wird, sind möglicherweise ausführlichere Informationen verfügbar, abhängig von der Art des Fehlers. Die COMAdmin-Objekte bieten erweiterte Informationen in Situationen, in denen die genaue Ursache des Fehlers ohne einen detaillierten Bericht, z. b. mit mehreren Lese-und Schreibvorgängen, schwer zu bestimmen ist.

Wenn Sie z. b. [**Methoden wie "auffüllen" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) " für ein [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt verwenden, können Sie Daten für jedes Element in der Sammlung lesen oder schreiben. Komplizierte Fehler können auftreten, und Sie können auf Grundlage eines einzelnen numerischen Fehlercodes schwierig zu diagnostizieren sein. Aus diesem Grund werden durch die COMAdmin-Bibliothek Erweiterte Fehlerinformationen über eine spezielle Sammlung ausgegeben.

Wenn erweiterte Fehlerinformationen verfügbar sind, werden Sie in der [**errorInfo**](errorinfo.md) -Auflistung platziert, die mit der ursprünglichen Auflistung verknüpft ist, in der der Fehler aufgetreten ist. Um den Fehlerbericht abzurufen, rufen Sie die **errorInfo** -Auflistung ab, die mit der ursprünglichen Auflistung verknüpft ist, und untersuchen Sie die darin enthaltenen Elemente. Sie können die **errorInfo** -Auflistung mithilfe von [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**comadmincatalogcollection**](comadmincatalogcollection.md)abrufen und den zweiten Parameter leer lassen, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.

Wenn Sie eine Fehlermeldung erhalten, müssen Sie die [**errorInfo**](errorinfo.md) -Auflistung sofort für die Auflistung, bei der ein Fehler aufgetreten ist, erhalten und Auffüllen, ohne weitere Vorgänge für diese Sammlung auszuführen. Andernfalls wird die **errorInfo** -Auflistung zurückgesetzt, und der Fehler wird nicht ausführlich erläutert.

Die Elemente in der [**errorInfo**](errorinfo.md) -Auflistung machen die speziellen Fehler Berichterstattungs Eigenschaften majorref und MinorRef verfügbar, die die jeweilige Ursache des Fehlers detailliert beschreiben. Weitere Informationen finden Sie unter **errorInfo**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



