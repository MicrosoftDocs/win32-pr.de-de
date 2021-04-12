---
description: Das Synchronisierungs Attribut ist eine deklarative Eigenschaft, die angibt, welcher Synchronisierungstyp bei der Aktivierung der Komponenten angezeigt werden soll.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Werte der Synchronisierungs Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393042"
---
# <a name="synchronization-attribute-values"></a>Werte der Synchronisierungs Attribute

Das Synchronisierungs Attribut ist eine deklarative Eigenschaft, die angibt, welcher Synchronisierungstyp bei der Aktivierung der Komponenten angezeigt werden soll. Wenn Sie das Synchronisierungs Attribut einschließen, verarbeitet com+ die Details der Synchronisierung in Ihrem Auftrag. Sie müssen keine weiteren Aufrufe durchführen.

Abhängig von den Anforderungen kann ein Objekt die Synchronisierung des Aufrufers freigeben, eine neue Synchronisierung erfordern oder ohne Synchronisierung arbeiten.

Com+ bietet die folgenden Synchronisierungs Attributwerte:

-   **Deaktiviert.** Wenn Sie das Synchronisierungs Attribut deaktivieren, ignoriert com+ die Synchronisierungs Anforderungen der Komponente beim Bestimmen des Kontexts für das Objekt. Folglich kann das Objekt den Kontext (und die Synchronisierung) seines Aufrufers freigeben.

    Im Allgemeinen sollten Sie diesen Attribut Wert verwenden, wenn Sie wissen, dass die Komponente niemals auf einen Ressourcen-Manager zugreift. Wenn Sie COM-Komponenten zu com+ migrieren, müssen Sie das Synchronisierungs Attribut deaktivieren, um das gleiche Verhalten wie die nicht konfigurierte COM-Komponente zu erhalten. Eine nicht konfigurierte Komponente ist eine COM-Komponente, die nicht in einer COM+-Anwendung installiert wurde.

-   **Nicht unterstützt.** Ein Objekt mit diesem Wert nimmt unabhängig vom Status seines Aufrufers nie an einer Synchronisierung teil. Diese Einstellung ist nur für nicht transaktionale Komponenten verfügbar und verwendet nicht den [com+-Just-in-time (JIT)-Aktivierungs](com--just-in-time-activation.md) Dienst.

-   **Unterstützt.** Ein Objekt mit diesem Wert ist an der Synchronisierung beteiligt, wenn es vorhanden ist. Sie deklarieren diesen Wert, wenn ein Objekt in der Synchronisierung seines Aufrufers freigegeben werden soll, aber keine eigene Synchronisierung erfordern muss.

    Ein guter Grund zum Festlegen des Synchronisierungs Attributs auf unterstützt ist, dass diese Einstellung in Bezug auf die Systemressourcen kostengünstiger sein kann. Es ist jedoch schwieriger, die Komponente zu schreiben, da Sie vor gleichzeitigen aufrufen geschützt werden muss. Das Festlegen des Synchronisierungs Attributs auf unterstützt ist, dass unter bestimmten Umständen eine Instanz des Objekts so erstellt werden kann, dass Sie nicht synchronisiert ist. Wenn das Threading Modell der Komponente frei ist oder beides ist, müssen Sie die Instanzdaten mit einem Sperrungs Mechanismus schützen. Wenn das Threading Modell Apartment (STA) ist, müssen Sie die Instanzdaten nicht schützen.

-   **Erforderlich.** Wenn Sie dieses Attribut festlegen, stellt com+ sicher, dass alle aus der Komponente erstellten Objekte synchronisiert werden. Wenn com+ eine Instanz der Komponente erstellt, wird sichergestellt, dass immer nur ein Thread diese Instanz durchläuft.

    Wenn com+ ein Objekt aktiviert, prüft es den Synchronisierungs Status des Aufrufers. Wenn der Aufrufer synchronisiert ist, fließt com+ die Synchronisierungs Grenze des Aufrufers, um das neue-Objekt einzuschließen. Andernfalls beginnt com+ mit der Synchronisierung.

-   **Erfordert "neu".** Ein Objekt mit diesem Wert muss an einer neuen Synchronisierung teilnehmen, wobei com+ die Kontexte und Apartments im Namen aller an dem-Befehl beteiligten Komponenten verwaltet. Com+ initiiert automatisch eine neue Synchronisierung, die sich von der Synchronisierung des Aufrufers unterscheidet.

    Ein guter Grund zum Festlegen des Synchronisierungs Attributs auf erfordert neu, dass diese Einstellung es Ihnen ermöglicht, externe Aufrufe an eine Instanz der Komponente effizienter durchzuführen. Es werden jedoch auch Aufrufe zwischen dem Objekt und dem Objekt, das es erstellt hat, in Bezug auf die Systemressourcen verteuert.

    Nehmen Sie z. b. an, dass das Objekt und das Erstellerobjekt die gleiche Synchronisierungs Grenze gemeinsam verwenden. Wenn Client a das Creator-Objekt aufruft und Client B das-Objekt aufruft, muss der zweite Aufruf warten, bis der erste Aufruf abgeschlossen ist. Wenn Sie "New" (neu) festlegen, wird das Objekt in einer separaten Synchronisierungs Grenze erstellt. In diesem Fall können Aufrufe von anderen Objekten gleichzeitig verarbeitet werden. Aufrufe vom Creator-Objekt an Ihr Objekt erfordern jedoch mehr Systemressourcen, da Sie Synchronisierungs Grenzen überschreiten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Synchronisierungs Attributs](setting-the-synchronization-attribute.md)
</dt> <dt>

[Synchronisierungs Abhängigkeiten](synchronization-dependencies.md)
</dt> </dl>

 

 



