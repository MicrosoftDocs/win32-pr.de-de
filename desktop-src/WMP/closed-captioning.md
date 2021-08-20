---
title: Untertitelung
description: Untertitelung
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Objektmodell, Synchronized Accessible Media Interchange (SAMI)
- Objektmodell,Synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player Mobiler, synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Mobile ActiveX,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player,Migrieren von Untertiteln
- Windows Media Player Objektmodell, Smigrieren von Untertiteln
- Objektmodell, Migrieren von Untertiteln
- Windows Media Player Mobil,Migrieren von Untertiteln
- Windows Media Player ActiveX,Migrieren von Untertiteln
- Windows Media Player Mobile ActiveX-Steuerelement, Migrieren von Untertiteln
- ActiveX,Migrieren von Untertiteln
- Synchronisierter austauschbarer Medienaustausch (SAMI), Migrieren von Untertiteln
- SAMI (Synchronized Accessible Media Interchange), Migrieren von Untertiteln
- Migrationshandbuch,Synchronized Accessible Media Interchange (SAMI)
- Migrationshandbuch, Untertitel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa83cb5fb6735475a883986673c958db9642386bd8ce2c76151ddd6c2f23ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119599"
---
# <a name="closed-captioning"></a>Untertitelung

Das Windows Media Player 6.4 ActiveX-Steuerelement enthält einen integrierten Anzeigebereich für Untertitel, der SAMI-Untertitel (Synchronized Accessible Media Interchange) aktiviert und den Untertiteltext anzeigt. Das Windows Media Player 7 oder höher ermöglicht die Anzeige von SAMI-Untertiteln mithilfe eines **<DIV>** HTML-Elements. Beispiel:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Diese Technik bietet Ihnen vollständige Flexibilität, da Sie Ihre Webseite so entwerfen können, dass Untertitel auf benutzerdefinierte Weise angezeigt werden. Die Untertitelanzeige muss sich nicht mehr an einem festen Ort neben der benutzeroberfläche Windows Media Player befinden.

Nachdem Sie einen Bereich zum Anzeigen von Untertiteln erstellt haben, verwenden Sie *closedCaption*. **captioningID-Eigenschaft,** um die Position anzugeben, an der Windows Media Player Untertiteltext rendert.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Das Windows Media Player Software Development Kit (SDK) enthält ein funktionierendes Beispiel für einen eingebetteten Player, der Untertiteltext anzeigt. Um die SDK-Beispiele zu erhalten, laden Sie das vollständige Windows Media Player SDK von der Microsoft-Website herunter, und installieren Sie es. Weitere Informationen zu Untertiteln und SAMI finden Sie auf der [Microsoft-Website für Barrierefreiheit.](https://www.microsoft.com/enable/)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Leitfaden zur Objektmodellmigration**](object-model-migration-guide.md)
</dt> </dl>

 

 




