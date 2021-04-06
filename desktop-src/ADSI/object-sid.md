---
title: Objekt-sid (WinNT-Anbieter)
description: Die Benutzer Sicherheits-ID (SID) kann mithilfe des Attributs "objectSID" abgerufen werden. Die objectSID wird als ein Variant-Array von Zeichen zurückgegeben, die die SID-Zeichenfolge bilden.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Objekt-sid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036310"
---
# <a name="object-sid-winnt-provider"></a>Objekt-sid (WinNT-Anbieter)

Die Benutzer Sicherheits-ID (SID) kann mithilfe des Attributs " **objectSID** " abgerufen werden. Die **objectSID** wird als ein **Variant** -Array von Zeichen zurückgegeben, die die SID-Zeichenfolge bilden.

## <a name="example-code"></a>Beispielcode


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




