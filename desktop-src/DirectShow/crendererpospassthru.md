---
description: Die crendererpospassthru-Klasse verarbeitet Such Befehle für rendererfilter, indem Sie vom Upstream an den nächsten Filter übergeben werden.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Crendererpospassthru-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360399"
---
# <a name="crendererpospassthru-class"></a>Crendererpospassthru-Klasse

![crendererpospassthru-Klassenhierarchie](images/cutil14.png)

Die- `CRendererPosPassThru` Klasse verarbeitet Such Befehle für rendererfilter, indem Sie vom Upstream an den nächsten Filter übergeben werden.

Diese Klasse wird von der [**cpospassthru**](cpospassthru.md) -Klasse abgeleitet. Es fügt Unterstützung für das Zwischenspeichern der Zeitstempel aus den Stichproben hinzu Verwenden Sie diese Klasse auf die gleiche Weise wie die **cpospassthru** -Klasse. Ausführliche Informationen finden Sie in der **cpospassthru** -Dokumentation.

Der rendererfilter muss die `CRendererPosPassThru` zwischengespeicherten Zeitstempel des Objekts wie folgt aktualisieren:

-   Für jedes Beispiel, das der Filter empfängt, wird die [**crendererpospassthru:: registermediatime**](crendererpospassthru-registermediatime.md) -Methode aufgerufen.
-   Wenn der Filter beendet wird oder einen **endflush** -Anruf empfängt, können Sie die [**crendererpospassthru:: resetmediatime**](crendererpospassthru-resetmediatime.md) -Methode aufrufen.
-   Wenn der Filter eine Benachrichtigung über das Ende des Datenstroms empfängt, wird die [**crendererpospassthru:: EOS**](crendererpospassthru-eos.md) -Methode aufgerufen.

Ein Beispiel für die Verwendung dieser Klasse finden Sie unter [**cbaserenderer**](cbaserenderer.md) -Quellcode.



| Öffentliche Methoden                                                            | BESCHREIBUNG                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Crendererpospassthru**](crendererpospassthru-crendererpospassthru.md) | Konstruktormethode.                                                 |
| [**Getmediatime**](crendererpospassthru-getmediatime.md)                 | Ruft die Zeitstempel im aktuellen Beispiel ab.                    |
| [**Registermediatime**](crendererpospassthru-registermediatime.md)       | Speichert die Zeitstempel aus dem aktuellen Beispiel zwischen.                     |
| [**Resetmediatime**](crendererpospassthru-resetmediatime.md)             | Setzt die zwischengespeicherten Zeitstempel auf NULL zurück.                              |
| [**Stereo**](crendererpospassthru-eos.md)                                   | Aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




