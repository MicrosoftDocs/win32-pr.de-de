---
description: Der Registrierungsschlüssel eudccoderange definiert Endbenutzer definierte Zeichen (EUDC)-Code Bereiche für verschiedene Codepages (Zeichensätze).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: Eudccoderange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352275"
---
# <a name="eudccoderange"></a>Eudccoderange

Der Registrierungsschlüssel eudccoderange definiert [Endbenutzer definierte Zeichen (EUDC)-](end-user-defined-characters.md) Code Bereiche für verschiedene Codepages (Zeichensätze). Sie wird nur von Tools verwendet, die eudcs erstellen, und ist nicht für EUDC-Benutzer von Bedeutung. Dieser Registrierungsschlüssel weist den folgenden Registrierungs Speicherort auf:

HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ nls \\ Codepage \\ eudccoderange

Das Format lautet:

Eudccoderange Codepage = FromTo \[ , FromTo\]

Dabei gilt:



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Eine der Zeichen folgen "932" (Japanisch), "936" (vereinfachtes Chinesisch), "949" (Koreanisch), "950" (traditionelles Chinesisch) oder "Unicode" (Unicode). Es werden keine anderen Werte unterstützt.                                     |
| FromTo   | Ein Zeichen folgen Wert, der aus einem Paar von vierstelligen hexadezimalen Werten besteht, die durch einen Bindestrich (-) getrennt sind. Es können bis zu vier FromTo-Werte angegeben werden, aber beide müssen vom vorherigen Wert durch ein Komma (,) getrennt werden. |



 

Im folgenden finden Sie die richtigen Werte für den Registrierungs Eintrag.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EUDC-Registrierungseinträge](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



