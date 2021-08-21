---
title: Bereiche
description: Bereiche
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Textdienstframework (TSF), Bereiche
- TSF (Textdienstframework),Bereiche
- Textdienste, Bereiche
- TSF-fähige Anwendungen, Bereiche
- ranges
- Textdienstframework (TSF), Anker
- TSF (Textdienstframework),Anchors
- Textdienste, Anker
- TSF-fähige Anwendungen, Anker
- Anker
- Textdienstframework (TSF), Klone
- TSF (Textdienstframework),Klone
- Textdienste,Klone
- TSF-fähige Anwendungen, Klone
- Klone
- Textdienstframework (TSF), Sicherungen
- TSF (Textdienstframework),Sicherungen
- Textdienste, Sicherungen
- TSF-fähige Anwendungen, Sicherungen
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215aabac226d664f1ec35a8302a8f6548d66337c8ab96f4799b58cc53216a7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951487"
---
# <a name="ranges"></a>Bereiche

## <a name="anchors"></a>Anchors

Ein Bereich wird durch zwei *Anker* getrennt, einen Startanker und einen Endanker. Ein Anker befindet sich in einem imaginären Slot zwischen zwei Zeichen. Der Startanker bezieht sich auf Text, der dem Anker folgt, und der Endanker bezieht sich auf Text, der dem Anker vorausgeht. Sowohl der Startanker als auch der Endanker können an derselben Position vorhanden sein. In diesem Fall hat der Bereich die Länge 0 (null).

Beginnen Sie beispielsweise mit folgendem Text:


```C++
This is text.
```



Wenden Sie nun einen Bereich auf diesen Text an, wobei sowohl der Startanker als auch der Endanker an Position 0 liegen. Sie wird visuell dargestellt als:


```C++
<anchor></anchor>This is text.
```



Die Anker nehmen keinen Platz innerhalb des Texts selbst ein. Dies ist ein Bereich der Länge 0 (null), und sein Text ist leer.

Verschieben Sie nun den Endanker um +3 Positionen. Sie wird visuell dargestellt als:


```C++
<anchor>Thi</anchor>s is text.
```



Der Startanker wird direkt vor dem Zeichen an Position 0 positioniert, und der Endanker wird direkt hinter dem Zeichen an Position 3 positioniert, da der Endanker an drei Stellen nach rechts verschoben wurde. Der Textbereich ist jetzt "Thi".

Darüber hinaus kann der Startanker nicht so erstellt werden, dass er dem Endanker folgt, und der Endanker kann nicht vor dem Startanker stehen.

## <a name="anchor-gravity"></a>Anchor-Schwerkraft

Jeder Anker verfügt über eine *Schwerkrafteinstellung,* die bestimmt, wie der Anker reagiert, wenn Text an der Ankerposition in den Textstream eingefügt wird. Wenn eine Einfügung an der Position eines Ankers erfolgt, muss eine Anpassung an der Position des Ankers vorgenommen werden. Die Schwerkraft bestimmt, wie diese Ankerpositionsanpassung vorgenommen wird.

Beispiel:


```C++
It is <anchor></anchor>cold today.
```



Wenn das Wort "very" an der Bereichsposition eingefügt wird, kann der Startanker vor oder nach dem eingefügten Wort positioniert werden:


```C++
It is <anchor>very </anchor>cold today.
```



\- Oder –


```C++
It is very <anchor></anchor>cold today.
```



Die Ankerschwere gibt an, wie der Anker neu positioniert wird, wenn eine Einfügung an seiner Position erfolgt. Die Schwerkraft kann entweder *rückwärts* oder *vorwärts sein.*

Wenn der Anker die Schwerkraft rückwärts hat, bewegt sich der Anker beim Einfügen relativ zur Einfügemarke rückwärts, sodass der eingefügte Text dem Anker folgt:


```C++
It is <anchor>very </anchor>cold today.
```



Wenn der Anker über vorwärts gerichtete Schwerkraft verfügt, bewegt sich der Anker beim Einfügen (relativ zur Einfügemarke) vorwärts, sodass der eingefügte Text vor dem Anker steht:


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Klone und Sicherungen

Es gibt zwei Möglichkeiten, eine "Kopie" eines Bereichsobjekts zu erstellen. Die erste besteht darin, mit [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone)einen *Klon* des Bereichs zu erstellen. Die zweite besteht darin, mithilfe von [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup)eine *Sicherung* des Bereichs durchzuführen.

Ein Klon ist eine Kopie eines Bereichs, der keine statischen Daten enthält. Die Anker des Bereichs werden kopiert, aber der Klon deckt immer noch einen Textbereich innerhalb des Kontexts ab. Ein Klon ist in jeder Hinsicht ein Bereichsobjekt. Dies bedeutet, dass der Text und die Eigenschaften für einen geklonten Bereich dynamisch sind und sich ändern, wenn sich der Text und/oder die Eigenschaften des bereichs ändern, der durch den Klon abgedeckt wird.

Eine Sicherung speichert den Text und die Eigenschaften eines Bereichs zum Zeitpunkt der Sicherung als statische Daten. Eine Sicherung klont auch den ursprünglichen Bereich, sodass Änderungen an Größe und Position des ursprünglichen Bereichs nachverfolgt werden können. Dies bedeutet, dass der Text und die Eigenschaften für einen gesicherten Bereich statisch sind und sich nicht ändern, wenn sich der Text und/oder die Eigenschaften des bereichs ändern, der von der Sicherung abgedeckt wird.

Beispielsweise der folgende Bereich (pRange) innerhalb des Kontexts:


```C++
"This is some <pRange>text</pRange>."
```



Erstellen Sie nun einen Klon und eine Sicherung dieses Bereichs:


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



Die -Objekte enthalten nun Folgendes:


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Ändern Sie nun den Text von pRange:


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



Die -Objekte enthalten nun Folgendes:


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



Durch das Festlegen des Texts wurde der Text innerhalb des Kontexts geändert. Außerdem wurde der Endanker von pRange und pClone geändert. pClone enthält jetzt "andere Wörter", da der Text innerhalb des Bereichs geändert wurde und diese Änderungen von allen Bereichen nachverfolgt werden. Wenn sich der von pRange und pClone abgedeckte Text geändert hat, hat sich auch der Text von pClone geändert.

Der Text in pBackup hat sich nicht vom ursprünglichen pRange geändert, da die Daten (Text und Eigenschaften) in der Sicherung nicht mit dem Kontext verknüpft sind und separat gespeichert werden. Der in der Sicherung enthaltene Klon ändert sich tatsächlich, aber die Daten sind statisch.

Beim Wiederherstellen einer Sicherung kann die Sicherung auf den Klon innerhalb der Sicherung oder auf einen anderen Bereich vollständig angewendet werden. Um die Sicherung auf den Klon innerhalb der Sicherung anzuwenden, übergeben Sie **NULL** an [ITfRangeBackup::Restore,](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) wie im folgenden Codebeispiel gezeigt:


```C++
pBackup->Restore(ec, NULL);
```



Die -Objekte enthalten nun Folgendes:


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Um die Sicherung in einem anderen Bereich wiederherzustellen, übergeben Sie beim Aufrufen von **ITfRangeBackup::Restore** einen Zeiger auf das Bereichsobjekt. Der sicherte Text und die Eigenschaften werden auf den neuen Bereich angewendet. Wenn Sie beispielsweise das obige Beispiel vor dem **Wiederherstellungsaufruf** verwenden, wird pRange geändert, um dies zu veranschaulichen:


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



Die -Objekte enthalten nun Folgendes:


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Wenn der Endanker von pRange an die beiden linken Stellen verschoben wurde, hat sich der Endanker von pClone nicht geändert.

Stellen Sie nun die Sicherung mithilfe von pRange mit dem folgenden Codebeispiel wieder her:


```C++
pBackup->Restore(ec, pRange);
```



Die -Objekte enthalten nun Folgendes:


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



Der von pRange abgedeckte Text wurde durch "text" ersetzt, ein Teil des Texts, der von pClone abgedeckt wird, wurde geändert, und pBackup wurde entsprechend pRange geändert.

 

 




