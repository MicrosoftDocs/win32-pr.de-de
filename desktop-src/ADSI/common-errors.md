---
title: Häufige Fehler (ADSI)
description: Alle ADSI-spezifischen Fehler haben eine hexadezimale Form von 80005xxx. Die häufigsten Fehlercodes sind in der folgenden Tabelle aufgeführt.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "104314021"
---
# <a name="common-errors-adsi"></a>Häufige Fehler (ADSI)

Alle ADSI-spezifischen Fehler haben eine hexadezimale Form von 80005xxx. Die häufigsten Fehlercodes sind in der folgenden Tabelle aufgeführt.



| ADSI Hex-Fehlercode | BESCHREIBUNG                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Es wurde ein ungültiger ADSI-Pfadname übermittelt. Dieser Fehler ergibt sich aus der Übergabe eines schlecht formatierten ADsPath an **GetObject** beim Binden an ein-Objekt.<br/> |
| 8000500D<br/> | Die ADSI-Eigenschaft wurde im Eigenschaften Cache nicht gefunden.<br/>                                                                                 |
| 8000500e<br/> | Das ADSI-Objekt ist vorhanden. Wenn Sie versuchen, ein ADSI-Objekt mit dem gleichen Namen wie ein vorhandenes ADSI-Objekt zu erstellen, tritt dieser Fehler auf.<br/>    |



 

Eine umfassende Liste der ADSI-Fehlercodes finden Sie unter [generische ADSI-Fehlercodes](generic-adsi-error-codes.md).

## <a name="com-errors"></a>COM-Fehler

Da ADSI aus COM-Objekten besteht, werden Standard-COM-Fehlercodes zurückgegeben. In der folgenden Tabelle sind die com-Fehlercodes aufgelistet, die in der ADSI-Programmierung am häufigsten auftreten.



| COM-Hex-Fehlercode  | BESCHREIBUNG                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Unbekannter Fehler. Die Ursache des COM-Objekt Fehlers ist von ADSI unbestimmt. <br/>                                  |
| 800041e4<br/> | Objekt konnte nicht gefunden werden. Dieser Fehler tritt hauptsächlich auf, wenn die ADsPath-Zeichenfolge beim Binden an ein-Objekt falsch geschrieben wird.<br/> |



 

Weitere Beispiele für COM-Fehler, die möglicherweise bei der ADSI-Programmierung auftreten, finden Sie unter [generische com-Fehler Codes](generic-com-error-codes.md) .

## <a name="win32-errors"></a>Win32-Fehler

Jeder Fehlercode der hexadezimalen Form 8007xxxx ist ein standardmäßiger Win32-Fehlercode. Wenn Sie die letzten vier Ziffern von "hexadezimal" in "Decimal" konvertieren, können Sie über die Windows 2000-Befehlszeile auf den Fehler zugreifen:

**net helpmsg <number>**

In der obigen Befehlszeile ist " &lt; Number &gt; " die Dezimalzahl, die durch die typumrechnung der letzten vier Ziffern des Fehlercodes aus dem Hexadezimalwert abgerufen wird. Diese Befehlszeile enthält eine ausführlichere Beschreibung des Win32-Fehlers, der beim Debuggen des Skripts sehr hilfreich sein kann.

 

 





