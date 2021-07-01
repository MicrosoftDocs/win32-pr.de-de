---
description: Der Registrierungsschlüssel EUDCCodeRange definiert EUDC-Codebereiche (End-User-Defined Character) für verschiedene Codepages (Zeichensätze).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120675"
---
# <a name="eudccoderange"></a>EUDCCodeRange

Der Registrierungsschlüssel EUDCCodeRange definiert [EUDC-Codebereiche (End-User-Defined Character)](end-user-defined-characters.md) für verschiedene Codepages (Zeichensätze). Sie wird nur von Tools verwendet, die EUDCs erstellen, und ist für EUDC-Benutzer nicht direkt von Bedeutung. Dieser Registrierungsschlüssel hat den folgenden Registrierungsspeicherort:

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

Das Format lautet:

EUDCCodeRange CodePage=FromTo \[ , FromTo\]

Dabei gilt:



| Wert         | BESCHREIBUNG                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Eine der Zeichenfolgen "932" (Japanisch), "936" (vereinfachtes Chinesisch), "949" (Koreanisch), "950" (traditionelles Chinesisch) oder "Unicode" (Unicode). Es werden keine anderen Werte unterstützt.                                     |
| FromTo   | Zeichenfolgenwert, der aus einem Paar aus vierstelligen Hexadezimalwerten besteht, getrennt durch einen Bindestrich (-). Bis zu vier FromTo-Werte können angegeben werden, aber jeder muss durch ein Komma (,) vom vorherigen Wert getrennt werden. |



 

Im Folgenden sind die richtigen Werte für den Registrierungseintrag angegeben.


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

 

 



