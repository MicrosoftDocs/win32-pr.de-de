---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e683bb441642e8f9764ac0cfe8313d0aa0df92ae3276f986f5fdf6837d6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795920"
---
# <a name="ajax"></a>AJAX

AJAX-Features in Windows Internet Explorer 8 wie [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) und [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) verfügen über native Eigenschaften, die mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen können.

Windows Internet Explorer macht neue Eigenschaften für bestimmte AJAX-Features verfügbar, z. [B. Dokumentübergreifendes Messaging (Cross-Document Messaging, XDM),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)auch in Kompatibilitätsansicht. Wenn Sie dem Ereignisobjekt benutzerdefinierte Eigenschaften hinzufügen, können diese mit diesen neuen Eigenschaften in Konflikt geraten, z. B. **mit der Quelle**.

Das folgende Codebeispiel funktioniert in älteren Versionen von Internet Explorer, aber nicht in neueren Versionen, da neue Features die **Source-Eigenschaft** verwenden.


```JScript
event.source = myObject;
```



Das folgende Codebeispiel zeigt, wie Sie dieses Objekt ändern können, um kompatibel zu bleiben.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



