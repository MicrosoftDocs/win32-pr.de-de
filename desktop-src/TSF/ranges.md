---
title: Bereiche
description: Bereiche
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Dienst Framework (TSF), Bereiche
- TSF (Text Dienst Framework), Bereiche
- Text Dienste, Bereiche
- TSF-aktivierte Anwendungen, Bereiche
- ranges
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- Text Dienste, Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
- Text Dienst Framework (TSF), Klone
- TSF (Text Dienst Framework), Klone
- Text Dienste, Klone
- TSF-aktivierte Anwendungen, Klone
- klässler
- Text Dienst Framework (TSF), Sicherungen
- TSF (Text Dienst Framework), Sicherungen
- Text Dienste, Sicherungen
- TSF-aktivierte Anwendungen, Sicherungen
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948056"
---
# <a name="ranges"></a>Bereiche

## <a name="anchors"></a>Anchors

Ein Bereich wird durch zwei *Anker*, einen Start Anker und einen endanker getrennt. Ein Anker ist in einem imaginären Slot zwischen zwei Zeichen vorhanden. Der Start Anker bezieht sich auf Text, der auf den Anker folgt, und der endanker bezieht sich auf Text, der dem Anker vorangestellt ist. Der Start-und der endanker können am gleichen Speicherort vorhanden sein. In diesem Fall hat der Bereich eine Länge von 0 (null).

Beginnen Sie z. b. mit folgendem Text:


```C++
This is text.
```



Wenden Sie nun einen Bereich auf diesen Text mit dem Start-und endanker an Position 0 an. Sie wird visuell wie folgt dargestellt:


```C++
<anchor></anchor>This is text.
```



Die Anker beanspruchen keinen Platz im Text selbst. Dies ist ein Bereich der Länge 0 (null), und der zugehörige Text ist leer.

Verschieben Sie nun die endanker + 3 Positionen. Sie wird visuell wie folgt dargestellt:


```C++
<anchor>Thi</anchor>s is text.
```



Der Start Anker wird direkt vor dem Zeichen an Position 0 positioniert, und der endananker wird direkt hinter das Zeichen an Position 3 positioniert, da der endenanchor an die drei Positionen verschoben wurde. Der Textbereich ist jetzt "Thi".

Darüber hinaus kann der Start Anker nicht so fest gemacht werden, dass er auf den Enden Anker folgt, und der endanker kann nicht vor dem Start Anker stehen.

## <a name="anchor-gravity"></a>Anker Schwergewicht

Jeder Anker verfügt über eine *schwere* Grad Einstellung, die bestimmt, wie der Anker antwortet, wenn Text an der Ankerposition in den Textstream eingefügt wird. Wenn eine Einfügung an der Position eines Ankers erfolgt, muss an der Position des Ankers eine Anpassung vorgenommen werden. Die Schwerkraft bestimmt, wie diese Anker Positions Anpassung vorgenommen wird.

Beispiel:


```C++
It is <anchor></anchor>cold today.
```



Wenn das Wort "very" an der Bereichs Position eingefügt wird, kann der Start Anker entweder vor oder nach dem eingefügten Wort positioniert werden:


```C++
It is <anchor>very </anchor>cold today.
```



\- Oder –


```C++
It is very <anchor></anchor>cold today.
```



Die Anker Gravitation gibt an, wie der Anker neu positioniert wird, wenn an seiner Position eine Einfügung vorgenommen wird. Die Schwerkraft kann entweder *rückwärts* oder *Vorwärts* sein.

Wenn der Anker eine abwärts Gravitation hat, wird der Anker nach hinten verschoben, relativ zur Einfügemarke, sodass der eingefügte Text dem Anker folgt:


```C++
It is <anchor>very </anchor>cold today.
```



Wenn der Anker eine vorwärts Gravitation hat, wechselt der Anker (relativ zur Einfügemarke) beim Einfügen, sodass der eingefügte Text vor dem Anker liegt:


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Klone und Sicherungen

Es gibt zwei Möglichkeiten, eine "Kopie" eines Range-Objekts zu erstellen. Der erste besteht darin, einen *Klon* des Bereichs mithilfe von " [itfrange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone)" zu erstellen. Die zweite besteht darin, eine *Sicherung* des Bereichs mithilfe von [ITfContext:: "" ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup)"" zu erstellen.

Ein Klon ist eine Kopie eines Bereichs, der keine statischen Daten enthält. Die Anker des Bereichs werden kopiert, aber der Klon deckt weiterhin einen Textbereich innerhalb des Kontexts ab. Ein Klon ist in jeder Hinsicht ein Bereichs Objekt. Dies bedeutet, dass der Text und die Eigenschaften für einen geklonten Bereich dynamisch sind und sich ändern, wenn sich der Text und/oder die Eigenschaften des vom Klon abgedeckten Bereichs ändern.

Eine Sicherung speichert den Text und die Eigenschaften eines Bereichs zu dem Zeitpunkt, zu dem die Sicherung als statische Daten erstellt wird. Eine Sicherung klont auch den ursprünglichen Bereich, sodass Änderungen an der Größe und Position des ursprünglichen Bereichs nachverfolgt werden können. Dies bedeutet, dass der Text und die Eigenschaften für einen gesicherten Bereich statisch sind und sich nicht ändern, wenn sich der Text und/oder die Eigenschaften des von der Sicherung behandelten Bereichs ändern.

Beispielsweise der folgende Bereich (Prange) innerhalb des Kontexts:


```C++
"This is some <pRange>text</pRange>."
```



Erstellen Sie jetzt einen Klon und eine Sicherung dieses Bereichs:


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



Nun enthalten die Objekte Folgendes:


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Ändern Sie nun den Text von Prange:


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



Nun enthalten die Objekte Folgendes:


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



Das Festlegen des Texts hat bewirkt, dass der Text im Kontext geändert wird. Außerdem wurde die Änderung des enden Ankers von Prange und pclone bewirkt. pclone enthält jetzt "andere Wörter", da sich der Text innerhalb des Bereichs geändert hat und diese Änderungen von allen Bereichen nachverfolgt werden. Wenn sich der von "Prange" und "pclone" behandelte Text geändert hat, wurde auch der Text des pclone geändert.

Der Text in pbackup wurde nicht vom ursprünglichen Prange geändert, da die Daten (Text und Eigenschaften) in der Sicherung nicht mit dem Kontext verknüpft sind und separat gespeichert werden. Der in der Sicherung enthaltene Klon ändert sich tatsächlich, aber die Daten sind statisch.

Beim Wiederherstellen einer Sicherung kann die Sicherung auf den Klon innerhalb der Sicherung oder auf einen anderen Bereich vollständig angewendet werden. Um die Sicherung auf den Klon innerhalb der Sicherung anzuwenden, übergeben Sie **null** an [itfrangebackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , wie im folgenden Codebeispiel gezeigt:


```C++
pBackup->Restore(ec, NULL);
```



Nun enthalten die Objekte Folgendes:


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Wenn Sie die Sicherung in einem anderen Bereich wiederherstellen möchten, übergeben Sie beim Aufrufen von **itfrangebackup:: Restore** einen Zeiger auf das Bereichs Objekt. Der gesicherte Text und die Eigenschaften werden auf den neuen Bereich angewendet. Beispielsweise wird für die Verwendung des obigen Beispiels vor dem **Wiederherstellungs** Vorgang Prange geändert, um Folgendes zu veranschaulichen:


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



Nun enthalten die Objekte Folgendes:


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Wenn der endanker von Prange an zwei Stellen verschoben wurde, hat sich der Endpunkt des pclone nicht geändert.

Stellen Sie nun die Sicherung mithilfe von Prange mit dem folgenden Codebeispiel wieder her:


```C++
pBackup->Restore(ec, pRange);
```



Nun enthalten die Objekte Folgendes:


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



Der von Prange abgedeckte Text wurde durch "Text" ersetzt, ein Teil des von pclone abgedeckten Texts hat sich geändert, und pbackup ändert sich entsprechend der Prange.

 

 




