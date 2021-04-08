---
title: Die UUID wird erzeugt.
description: Der erste Schritt beim Definieren der Schnittstelle ist die Verwendung des Hilfsprogramms "uuidgen, um einen universellen eindeutigen Bezeichner (UUID) zu generieren.
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Remote Prozedur Aufruf RPC, Tasks, erzeugen der UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856067"
---
# <a name="generating-the-uuid"></a>Die UUID wird erzeugt.

Der erste Schritt beim Definieren der Schnittstelle ist die Verwendung des Hilfsprogramms **"uuidgen** , um einen universellen eindeutigen Bezeichner (UUID) zu generieren. Eine UUID ermöglicht es Client-und Server Anwendungen, sich gegenseitig zu identifizieren. Das Hilfsprogramm **"uuidgen** (Uuidgen.exe) wird automatisch installiert, wenn Sie das Platform Software Development Kit (SDK) installieren.

Mit dem folgenden Befehl wird eine UUID generiert und eine Vorlagen Datei mit dem Namen "Hello. idl" erstellt.

**"uuidgen/i/ohello.idl**

Die Vorlage "Hello. idl" sieht wie folgt aus (mit einer anderen UUID).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




