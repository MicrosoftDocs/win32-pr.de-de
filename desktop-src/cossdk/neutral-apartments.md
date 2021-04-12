---
description: Mit com+ werden neutrale Apartments eingeführt, um die Programmierung in Multithreadumgebungen zu vereinfachen. Das neutrale Apartment ist das bevorzugte Modell für com+ für Komponenten ohne Benutzeroberfläche.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Neutrale Apartments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393069"
---
# <a name="neutral-apartments"></a>Neutrale Apartments

Mit com+ werden neutrale Apartments eingeführt, um die Programmierung in Multithreadumgebungen zu vereinfachen. Das neutrale Apartment ist das bevorzugte Modell für com+ für Komponenten ohne Benutzeroberfläche.

In der Vergangenheit mussten com+-Entwickler, die Server Skalierbarkeit erforderten, kostenlose Thread Komponenten implementieren, um Engpässe zu vermeiden. das Implementieren von kostenlosen Threading Modellen ist jedoch komplizierter, da Sie mit dem Zugriff auf die Sperre umgehen müssen. In neutralen Apartments befolgen Objekte die Richtlinien für multithreadwohnungen, können aber auch in jeder Art von Thread ausgeführt werden. Wenn ein Thread in einem neutralen Apartment ausgeführt wird, wird der Kontext des Objekts ohne einen Thread Wechsel empfangen.

Jeder Prozess kann nur über ein neutrales Apartment verfügen. Verwenden Sie die folgende Registrierungs Einstellung, um ein neutrales Apartment auszuwählen:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

Komponenten mit Benutzeroberflächen sollten Single Thread-Apartments weiterhin als bevorzugtes Modell verwenden. Verwenden Sie die folgende Registrierungs Einstellung, um ein Single Thread-Apartment auszuwählen:

**ThreadingModel** = Apartment

 

 



