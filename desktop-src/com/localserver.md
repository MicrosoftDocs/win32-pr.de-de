---
title: LocalServer
description: Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Registrierungsschlüssel für LocalServer com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037306"
---
# <a name="localserver"></a>LocalServer

Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der den vollständigen Pfad angibt und beliebige Befehlszeilenargumente enthalten kann.

COM fügt das Flag "-Einbettungs" an die Zeichenfolge an, sodass die Anwendung, die Flags verwendet, die gesamte Zeichenfolge analysieren und nach dem-Einbettungs Flag suchen muss.

Um einen COM-Objekt Server in einem separaten Speicherbereich auszuführen, ändern Sie den Wert von **LocalServer** wie folgt:

**cmd/c Start/separate** *Path * * *. exe**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




