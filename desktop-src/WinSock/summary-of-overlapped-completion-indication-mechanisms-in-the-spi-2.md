---
description: Zusammenfassung der überlappenden Vervollständigungs Anzeige Mechanismen im SPI von Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Zusammenfassung der Überlapp enden Vervollständigungs Anzeige Mechanismen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129116"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Zusammenfassung der Überlapp enden Vervollständigungs Anzeige Mechanismen in der SPI

In der folgenden Tabelle wird die Vervollständigungs Semantik für einen überlappenden Socket zusammengefasst, wobei die verschiedenen Kombinationen von *lpoverllapp*, **hevent** und *lpCompletionRoutine* angezeigt werden.



| *lpoverlgetauscht* | **hevent**     | *lpCompletionRoutine* | Vervollständigungs Angabe                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Nicht verfügbar | Wird ignoriert.               | Der Vorgang wird synchron abgeschlossen, d. h. er verhält sich wie ein nicht überlappenden Socket.                                                                                                                                 |
| nicht NULL       | NULL           | NULL                  | Der Vorgang wird überlappen abgeschlossen, aber es gibt keinen von Windows Sockets 2 unterstützten Abschlussmechanismus. Der Mechanismus für den Abschluss Port (falls unterstützt) kann in diesem Fall verwendet werden, andernfalls wird keine Vervollständigungs Benachrichtigung angezeigt. |
| nicht NULL       | nicht NULL       | NULL                  | Der Vorgang wird überlappende Benachrichtigungen durch Signalisieren von Ereignis Objekten abgeschlossen.                                                                                                                                                      |
| nicht NULL       | Wird ignoriert.        | nicht NULL              | Der Vorgang wird überlappende Benachrichtigungen durch Planen der Abschluss Routine abgeschlossen.                                                                                                                                               |



 

 

 



