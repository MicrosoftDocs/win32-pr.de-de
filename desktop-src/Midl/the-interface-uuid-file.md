---
title: Die UUID-Schnittstellen Datei
description: Die UUID-Schnittstellen Datei sammelt die Definitionen der Schnittstellen Bezeichner von allen Schnittstellen in der verarbeiteten IDL-Datei.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- Mittel l und com-Mittell, Schnittstellen, Proxy-UUID-Dateien
- Schnittstellen-UUID-Datei (Mitte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713457"
---
# <a name="the-interface-uuid-file"></a>Die UUID-Schnittstellen Datei

Die UUID-Schnittstellen Datei sammelt die Definitionen der Schnittstellen Bezeichner von allen Schnittstellen in der verarbeiteten IDL-Datei. Ähnlich wie bei der Stubdatei und der Header Datei wird die Eingabedaten Stromsperre durch die aktuelle IDL-Datei und die enthaltenen Dateien definiert. Beispielsweise generiert der Compiler für Interface iface eine Konstante IID \_ iface und initialisiert sie mit der in der IDL-Datei angegebenen UUID der Schnittstelle. Client Anwendungen und die Proxy-dll verwenden diese Konstante, um die Schnittstelle zu identifizieren.

Der Standardname für eine Schnittstellen-IID-Datei, die aus einer Datei erstellt wird. idl ist File \_ i.c. Der [**/IID**](-iid.md) -Compilerschalter überschreibt den Standardnamen der Schnittstellen-UUID-Datei.

 

 




