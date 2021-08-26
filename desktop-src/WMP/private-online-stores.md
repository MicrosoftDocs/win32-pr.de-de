---
title: Private Onlineshops
description: Private Onlineshops
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Onlineshops, privat
- Onlineshops, privat
- Geben Sie 1 Onlineshops ein, privat.
- Geben Sie 2 Onlineshops ein, privat.
- private Onlineshops
- Registrierung, private Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0667c19ffde3bb3c78b539253650e4f6f0b84cfbfd940f4d06237f987b99efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002930"
---
# <a name="private-online-stores"></a>Private Onlineshops

Windows Media Player 10 oder höher unterstützt private Onlineshops. Das heißt, Speicher, die nur für bestimmte Benutzer sichtbar sind. Damit ein privater Onlineshop für den aktuellen Benutzer sichtbar ist, muss ein Eintrag vorhanden sein, der den privaten Onlineshop unter dem folgenden Registrierungsschlüssel darstellt.

HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ PrivateServices

Der erforderliche Registrierungseintrag muss das folgende Format aufweisen.



| Name                                                         | type           | Wert                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Beliebiger Name, der von der Person ausgewählt wird, die den Registrierungseintrag erstellt | **REG \_ DWORD** | Eine von Microsoft bereitgestellte Zahl, die den privaten Onlineshop identifiziert. |



 

Das Windows Media Player 10 ActiveX-Steuerelement unterstützt private Onlineshops nur, wenn das Steuerelement im Remotemodus ausgeführt wird. Das Windows Media Player 11 ActiveX-Steuerelement unterstützt private Onlineshops, unabhängig davon, ob das Steuerelement im Remotemodus ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




