---
title: PreferredServerBitness
description: Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen COM-Server fest.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- PreferredServerBitness-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b003fd4bdd861cbfd82e249123831e4e017eaeef1ad76b95121244fd415ae0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309985"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen COM-Server fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert,** der nur in 64-Bit-Versionen von Windows verfügbar ist.



| Wert | Beschreibung                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Passen Sie die Serverarchitektur der Clientarchitektur an. Wenn der Client beispielsweise 32-Bit ist, verwenden Sie eine 32-Bit-Version des Servers, sofern verfügbar. Falls nicht, schlägt die Aktivierungsanforderung des Clients fehl. |
| 2     | Verwenden Sie eine 32-Bit-Version des Servers. Wenn keine vorhanden ist, schlägt die Aktivierungsanforderung des Clients fehl.                                                                                                      |
| 3     | Verwenden Sie eine 64-Bit-Version des Servers. Wenn keine vorhanden ist, schlägt die Aktivierungsanforderung des Clients fehl.                                                                                                      |



 

Wenn dieser Wert nicht vorhanden ist, geschieht Folgendes:

-   Wenn auf dem Computer, auf dem der Server hostet, Windows XP oder Windows Server 2003 ohne Installation von SP1 oder höher ausgeführt wird, bevorzugt COM eine 64-Bit-Version des Servers, falls verfügbar. Andernfalls wird eine 32-Bit-Version des Servers aktiviert.
-   Wenn auf dem Computer, der den Server hostet, Windows Server 2003 mit installiertem SP1 oder höher ausgeführt wird, versucht COM, die Serverarchitektur mit der Clientarchitektur abzugleichen. Anders ausgedrückt: Für einen 32-Bit-Client aktiviert COM einen 32-Bit-Server, sofern verfügbar. Andernfalls wird eine 64-Bit-Version des Servers aktiviert. Für einen 64-Bit-Client aktiviert COM einen 64-Bit-Server, sofern verfügbar. Andernfalls wird ein 32-Bit-Server aktiviert.

Der Client kann auch seine eigene Architekturpräferenz über die FLAGS CLSCTX \_ ACTIVATE \_ 32 \_ BIT SERVER und \_ CLSCTX \_ ACTIVATE \_ 64 \_ BIT SERVER \_ angeben. Dadurch wird die Einstellung des Servers überschrieben. Weitere Informationen und ein Diagramm der möglichen Interaktionen zwischen Client- und Serverarchitektureinstellungen finden Sie unter [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 