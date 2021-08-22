---
title: Generieren der UUID
description: Der erste Schritt beim Definieren der Schnittstelle besteht darin, das Hilfsprogramm uuidgen zu verwenden, um einen universally unique identifier (UUID) zu generieren.
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Remoteprozeduraufruf RPC , Tasks, Generieren der UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929527"
---
# <a name="generating-the-uuid"></a>Generieren der UUID

Der erste Schritt beim Definieren der Schnittstelle besteht darin, das **Hilfsprogramm uuidgen** zu verwenden, um einen universally unique identifier (UUID) zu generieren. Mit einer UUID können sich Client- und Serveranwendungen gegenseitig identifizieren. Das **Hilfsprogramm uuidgen** (Uuidgen.exe) wird automatisch installiert, wenn Sie das Platform Software Development Kit (SDK) installieren.

Der folgende Befehl generiert eine UUID und erstellt eine Vorlagendatei namens Hello.idl.

**uuidgen /i /ohello.idl**

Ihre hello.idl-Vorlage sieht wie folgt aus (natürlich mit einer anderen UUID).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




