---
description: Die dvddirectory-Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Dvddirectory (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860280"
---
# <a name="dvddirectory-property"></a>Dvddirectory (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDDirectory` Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeichen folgen Wert zurück, der den Pfad zum DVD-Stammverzeichnis angibt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Verwenden Sie diese Methode, um den Stammpfad festzulegen, wenn mehr als ein DVD-Laufwerk auf einem System vorhanden ist. Wenn nur ein Laufwerk auf dem System vorhanden ist und der Laufwerk Buchstabe höher als "C" ist, findet das mswebdvd-Objekt es automatisch. Für eine Standard DVD-Video-CD sollte der Stammpfad das TS- \_ Video Verzeichnis enthalten:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Einige DVD-Volumes können Ihr Video in einem Verzeichnis mit dem Namen "Video \_ TS" enthalten. Die allgemeine Idee ist, dass ein zusätzliches "DVD-Volume" (der Satz von. IFO. VOB und. BUP-Dateien, die normalerweise im Verzeichnis "Video TS" gespeichert werden, \_ können in einem Unterverzeichnis auf der Festplatte abgelegt werden. Wenn Sie den Stamm so ändern, dass er auf dieses Verzeichnis verweist, wird mswebdvd auf diesem separaten DVD-Volume ausgeführt. Ein neuer Satz von Menüs, Titeln usw. ist unabhängig von den Titeln im Video TS-Stamm verfügbar, auf \_ die nicht mehr zugegriffen werden kann. Solche Verzeichnisse werden als "verborgene Verzeichnisse" bezeichnet. Im folgenden Beispiel wird gezeigt, wie ein ausgeblendetes Verzeichnis als Stamm festgelegt wird, wobei "Hidden" ein Platzhalter für den Namen ist, den die Autoren der CD dem Verzeichnis gegeben haben.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



