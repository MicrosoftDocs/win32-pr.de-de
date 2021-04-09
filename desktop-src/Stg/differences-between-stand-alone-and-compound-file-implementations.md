---
title: Unterschiede zwischen eigenständigen Implementierungen und Implementierungen von Verbund Dateien
description: Die eigenständige Implementierung der Eigenschaften Satz Schnittstellen und die Implementierung der Verbund Datei unterscheiden sich in gewisser Weise.
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage-Klasse "STG", Implementierungen
- "\"IPropertyStorage\", \"unctd STG\", Implementierungen, Unterschiede"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855947"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>Unterschiede zwischen eigenständigen Implementierungen und Implementierungen von Verbund Dateien

Die eigenständige Implementierung der Eigenschaften Satz Schnittstellen und die Implementierung der Verbund Datei unterscheiden sich in gewisser Weise. In der Implementierung der Verbund Datei von Stream, Speicher, Eigenschaften Satz Speicher und Eigenschaften Speicher Objekten werden die verschiedenen Schnittstellen untereinander koordiniert, da Sie eine gemeinsame Implementierung gemeinsam verwenden. In der eigenständigen Implementierung sind die Schnittstellen Implementierungen unterschiedlich.

Folglich behandelt die Implementierung von Verbund Dateien Parallelitäts Probleme und synchronisiert das Eigenschaften Satz Objekt mit dem Speicher-oder Streamobjekt. Bei der eigenständigen Implementierung ist der Client für die Behandlung von Parallelitäts-und Synchronisierungs Problemen zwischen dem Speicher-oder Streamobjekt und dem Eigenschaften Satz verantwortlich. Ein Client kann diese Anforderungen erfüllen, indem er zwei einfache Regeln folgt. Manipulieren Sie zunächst nie einen Eigenschaften Satz mithilfe der zugehörigen Datenstrom-oder Speicher Schnittstellen, während ein Eigenschafts Speicher Objekt geöffnet ist. Rufen Sie dann immer **Commit** für ein Eigenschaften Speicher Objekt auf, bevor Sie **CopyTo**-, **muveelementto**-oder **Commit** für ein Vorgänger Speicher Objekt aufrufen. Insbesondere die folgenden Elemente erfordern eine Client Aufmerksamkeit:

-   In der Implementierung der Verbund Datei bietet ein einzelner Mechanismus Parallelitäts Schutz für das Speicher Objekt und die zugehörigen Eigenschaften Satz Objekte. In der eigenständigen Implementierung ist die Implementierung des Speicher Objekts jedoch von der Implementierung der-Eigenschaften Menge getrennt, und jede stellt eigene Parallelitäts Mechanismen bereit. Daher ist der Client in der eigenständigen Implementierung für die Aufrechterhaltung des Parallelitäts Schutzes zwischen den beiden Implementierungen durch einen Mechanismus des gegenseitigen Ausschlusses verantwortlich.
-   In der Implementierung der Verbund Datei werden Änderungen an Eigenschafts Sätzen in einem Eigenschafts Satz Cache gepuffert. Wenn dann die [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) -Methode für das Speicher Objekt aufgerufen wird, leert die Implementierung der Verbund Dateien automatisch die Eigenschaften Satzänderungen aus dem Eigenschaften Satz Puffer, bevor ein Commit für das Speicher Objekt ausgeführt wird. Folglich werden die Eigenschaften Satzänderungen als Teil der Transaktion, für die ein Commit ausgeführt wird, sichtbar gemacht.

    In der eigenständigen Implementierung muss der Client den Eigenschafts Satz Puffer explizit leeren, indem er [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) anruft, bevor die [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) -Methode für den Speicher aufgerufen wird. Alternativ kann der Client den neuen propsetflag- \_ Wert in der eigenständigen Implementierung verwenden, um direkt in den Eigenschaften Satz zu schreiben, anstatt Änderungen am internen Puffer des Eigenschaften Satzes zwischenzuspeichern. Wenn propsetflag \_ nicht gepuffert wird, werden die Zuständigkeiten des Clients automatisch erfüllt. Der nicht gepufferte Wert propsetflag wird von der Implementierung der Verbund Datei nicht unterstützt \_ . Weitere Informationen finden Sie unter [**propsetflag-Konstanten**](propsetflag-constants.md).

-   Wie bei transaktiven Storages aktualisiert die Implementierung der Verbund Datei den Eigenschaften Satz, indem er den internen Puffer leert, bevor er einen [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) -oder [**IStorage:: muveelementto**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)-Befehl aufruft. Folglich werden Änderungen am Eigenschaften Satz im kopierten oder verschostellten Speicher Element widergespiegelt.

    In der eigenständigen Implementierung muss der-Client den Eigenschafts Satz Puffer explizit leeren, indem er [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) vor dem Aufrufen von [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) oder [**IStorage::-Element to**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)aufruft. Alternativ kann der Client den \_ nicht gepufferten Wert New propsetflag verwenden, um direkt in den Eigenschaften Satz zu schreiben, anstatt Änderungen am Eigenschaften Satz Puffer zwischenzuspeichern. Weitere Informationen finden Sie unter [**propsetflag-Konstanten**](propsetflag-constants.md).

 

 




