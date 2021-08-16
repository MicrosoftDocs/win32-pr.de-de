---
title: Häufige Fehler (ADSI)
description: Alle ADSI-spezifischen Fehler haben die Hexadezimalform 80005xxx. Die am häufigsten aufgetretenen Fehlercodes sind in der folgenden Tabelle aufgeführt.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efcbbbce67d9928c9ecda3840f34a1cbf6faae79ca4d9fe72830a5b57881177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692194"
---
# <a name="common-errors-adsi"></a>Häufige Fehler (ADSI)

Alle ADSI-spezifischen Fehler haben die Hexadezimalform 80005xxx. Die am häufigsten aufgetretenen Fehlercodes sind in der folgenden Tabelle aufgeführt.



| Hexadezimaler ADSI-Fehlercode | Beschreibung                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Ein ungültiger ADSI-Pfadname wurde übergeben. Dieser Fehler resultiert aus der Übergabe eines schlecht gebildeten ADsPath an **GetObject bei** der Bindung an ein Objekt.<br/> |
| 8000500D<br/> | Die ADSI-Eigenschaft wurde im Eigenschaftencache nicht gefunden.<br/>                                                                                 |
| 8000500E<br/> | Das ADSI-Objekt ist vorhanden. Wenn Sie versuchen, ein ADSI-Objekt mit dem gleichen Namen wie ein vorhandenes ADSI-Objekt zu erstellen, tritt dieser Fehler auf.<br/>    |



 

Eine vollständige Liste der ADSI-Fehlercodes finden Sie unter [Generische ADSI-Fehlercodes](generic-adsi-error-codes.md).

## <a name="com-errors"></a>COM-Fehler

Da ADSI aus COM-Objekten besteht, werden standardmäßige COM-Fehlercodes zurückgegeben. In der folgenden Tabelle sind die COM-Fehlercodes aufgeführt, die am häufigsten bei der ADSI-Programmierung auftreten.



| COM-Hexadezimalfehlercode  | Beschreibung                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Unbekannter Fehler. Die Ursache des COM-Objektfehlers ist durch ADSI unbestimmt. <br/>                                  |
| 800041E4<br/> | Objekt konnte nicht gefunden werden. Dieser Fehler tritt hauptsächlich auf, weil die ADsPath-Zeichenfolge bei der Bindung an ein Objekt falsch geschrieben wurde.<br/> |



 

Weitere [Beispiele für COM-Fehler,](generic-com-error-codes.md) die bei der ADSI-Programmierung auftreten können, finden Sie unter Generische COM-Fehlercodes.

## <a name="win32-errors"></a>Win32-Fehler

Jeder Fehlercode der Hexadezimalform 8007xxxx ist ein Win32-Standardfehlercode. Wenn Sie die letzten vier Ziffern von hexadezimal in dezimal konvertieren, können Sie über die Befehlszeile Windows 2000 auf den Fehler zugreifen:

**net helpmsg <number>**

In der obigen Befehlszeile ist " number " die Dezimalzahl, die durch Konvertieren der letzten vier Ziffern des Fehlercodes aus &lt; &gt; hexadezimalen Zahlen ermittelt wird. Diese Befehlszeile enthält eine nützlichere Beschreibung des Win32-Fehlers, die beim Debuggen Ihres Skripts hilfreich sein kann.

 

 





