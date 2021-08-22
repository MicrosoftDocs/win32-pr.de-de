---
title: Objekt-SID (WinNT-Anbieter)
description: Die Benutzersicherheits-ID (SID) kann mithilfe des objectSID-Attributs abgerufen werden. Die objectSID wird als VARIANT-Array von Zeichen zurückgegeben, die die SID-Zeichenfolge bilden.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele, Objekt-SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331d1214e97ec6c751171f77e625a40395283b14d941ac1bb0775ea0c9efe27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391820"
---
# <a name="object-sid-winnt-provider"></a>Objekt-SID (WinNT-Anbieter)

Die Benutzersicherheits-ID (SID) kann mithilfe des **objectSID-Attributs abgerufen** werden. Die **objectSID wird** als **VARIANT-Array** von Zeichen zurückgegeben, die die SID-Zeichenfolge bilden.

## <a name="example-code"></a>Beispielcode


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




