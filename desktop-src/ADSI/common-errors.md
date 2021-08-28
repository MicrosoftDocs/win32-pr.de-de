---
title: Häufige Fehler (ADSI)
description: Alle ADSI-spezifischen Fehler weisen die Hexadezimalform 80005xxx auf. Die häufigsten aufgetretenen Fehlercodes sind in der folgenden Tabelle aufgeführt.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c0949d13139b132cd7c1a7a96ff6a95cd3b5e4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884065"
---
# <a name="common-errors-adsi"></a>Häufige Fehler (ADSI)

Alle ADSI-spezifischen Fehler weisen die Hexadezimalform 80005xxx auf. Die häufigsten aufgetretenen Fehlercodes sind in der folgenden Tabelle aufgeführt.



| ADSI-Hexadezimalfehlercode | Beschreibung                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Ein ungültiger ADSI-Pfadname wurde übergeben. Dieser Fehler tritt auf, wenn beim Binden an ein Objekt ein schlecht gebildeter ADsPath an **GetObject** übergeben wird.<br/> |
| 8000500D<br/> | Die ADSI-Eigenschaft kann nicht im Eigenschaftencache gefunden werden.<br/>                                                                                 |
| 8000500E<br/> | Das ADSI-Objekt ist vorhanden. Wenn Sie versuchen, ein ADSI-Objekt mit dem gleichen Namen wie ein vorhandenes ADSI-Objekt zu erstellen, tritt dieser Fehler auf.<br/>    |



 

Eine vollständige Liste der ADSI-Fehlercodes finden Sie unter [Generische ADSI-Fehlercodes.](generic-adsi-error-codes.md)

## <a name="com-errors"></a>COM-Fehler

Da ADSI aus COM-Objekten besteht, werden standardmäßige COM-Fehlercodes zurückgegeben. In der folgenden Tabelle sind die COM-Fehlercodes aufgeführt, die am häufigsten bei der ADSI-Programmierung auftreten.



| COM-Hexadezimalfehlercode  | Beschreibung                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Unbekannter Fehler. Die Ursache des COM-Objektfehlers ist von ADSI unbestimmt. <br/>                                  |
| 800041E4<br/> | Objekt konnte nicht gefunden werden. Dieser Fehler tritt hauptsächlich auf, weil die ADsPath-Zeichenfolge bei der Bindung an ein Objekt falsch geschrieben wurde.<br/> |



 

Weitere Beispiele für COM-Fehler, die bei der ADSI-Programmierung auftreten können, finden Sie unter [Generische COM-Fehlercodes.](generic-com-error-codes.md)

## <a name="win32-errors"></a>Win32-Fehler

Jeder Fehlercode im hexadezimalen Format 8007xxxx ist ein Win32-Standardfehlercode. Wenn Sie die letzten vier Ziffern von hexadezimal in decimal konvertieren, können Sie über die Windows 2000-Befehlszeile auf den Fehler zugreifen:

**net helpmsg &lt; number&gt;**

In der obigen Befehlszeile &lt; ist &gt; "number" die Dezimalzahl, die durch Konvertieren der letzten vier Ziffern des Fehlercodes aus hexadezimalen Zeichen abgerufen wurde. Diese Befehlszeile bietet eine nützlicheere Beschreibung des Win32-Fehlers, der beim Debuggen Ihres Skripts hilfreich sein kann.

 

 





