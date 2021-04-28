---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088758"
---
# <a name="ajax"></a>AJAX

AJAX-Features in Windows Internet Explorer 8 wie [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) und [Dokumentübergreifendes Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) verfügen über native Eigenschaften, die mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen können.

Windows Internet Explorer macht neue Eigenschaften für bestimmte AJAX-Features verfügbar, z. B. dokumentübergreifendes [Messaging (XDM),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)auch in Kompatibilitätsansicht. Wenn Sie dem Ereignisobjekt benutzerdefinierte Eigenschaften hinzufügen, können diese mit diesen neuen Eigenschaften in Konflikt stehen, z. B. **der Quelle**.

Das folgende Codebeispiel funktioniert in älteren Versionen von Internet Explorer jedoch nicht in neueren Versionen, da neue Features die **Quelleigenschaft** verwenden.


```JScript
event.source = myObject;
```



Das folgende Codebeispiel zeigt, wie Sie dieses Objekt ändern können, um kompatibel zu bleiben.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



