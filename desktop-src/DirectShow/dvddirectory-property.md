---
description: Die DVDDirectory-Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: DVDDirectory-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749100"
---
# <a name="dvddirectory-property"></a>DVDDirectory-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDDirectory` -Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeichenfolgenwert zurück, der den Pfad zum DVD-Stammverzeichnis angibt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Verwenden Sie diese Methode zum Festlegen des Stammpfads, wenn auf einem System mehrere DVD-Laufwerke enthalten sind. Wenn auf dem System nur ein Laufwerk installiert ist und sein Laufwerkbuchstaben höher als "C" ist, wird es vom MSWebDVD-Objekt automatisch gefunden. Bei einem standarden DVD-Video sollte der Stammpfad das Verzeichnis ts \_ video enthalten:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Einige DVD-Volumes enthalten ihr Video möglicherweise in einem Verzeichnis, das einen anderen Namen als "video \_ ts" hat. Die allgemeine Idee ist, dass ein zusätzliches "DVD-Volume" (der Satz von ) ist. Ifo. VOB und . BUP-Dateien, die normalerweise im Verzeichnis VIDEO TS gespeichert werden, können in einem Unterverzeichnis auf \_ dem Datenträger abgelegt werden. Durch Ändern des Stammverzeichnisses, um auf dieses Verzeichnis zu verweisen, wird MSWebDVD auf diesem separaten DVD-Volume betrieben. Unabhängig von den Titeln im VIDEO TS-Stamm ist eine neue Gruppe von Menüs, Titeln und so weiter verfügbar, auf die \_ nicht mehr zugegriffen werden kann. Solche Verzeichnisse werden als "ausgeblendete Verzeichnisse" bezeichnet. Das folgende Beispiel zeigt, wie Sie ein ausgeblendetes Verzeichnis als Stammverzeichnis festlegen, wobei "hidden" ein Platzhalter für den Namen ist, den die Datenträgerautoren dem Verzeichnis gegeben haben.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



