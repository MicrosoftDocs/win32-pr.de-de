---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960804"
---
# <a name="ajax"></a>AJAX

AJAX-Features in Windows Internet Explorer 8, wie [**XDR (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) und [Cross-Document Messaging (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , verfügen über systemeigene Eigenschaften, die möglicherweise mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen.

Windows Internet Explorer macht neue Eigenschaften für bestimmte AJAX-Features verfügbar, wie z. b. [Cross-Document Messaging (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), auch in der Kompatibilitäts Ansicht. Wenn Sie dem Ereignis Objekt benutzerdefinierte Eigenschaften hinzufügen, können Sie mit diesen neuen Eigenschaften, z. b. der **Quelle**, in Konflikt stehen.

Das folgende Codebeispiel funktioniert in älteren Versionen von Internet Explorer, aber nicht in neueren Versionen, da neue Features die **Source** -Eigenschaft verwenden.


```JScript
event.source = myObject;
```



Im folgenden Codebeispiel wird gezeigt, wie Sie dieses Objekt ändern können, damit es kompatibel bleibt.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



