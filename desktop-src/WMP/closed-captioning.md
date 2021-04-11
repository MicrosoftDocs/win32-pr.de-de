---
title: Untertitel
description: Untertitel
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player, Migrieren von Untertiteln
- Windows Media Player-Objektmodell, smigrieren von Untertiteln
- Objektmodell, Migrieren von Untertiteln
- Windows Media Player Mobile, Migrieren von Untertiteln
- Windows Media Player ActiveX-Steuerelement, Migrieren von Untertiteln
- Windows Media Player Mobile ActiveX-Steuerelement, Migrieren von Untertiteln
- ActiveX-Steuerelement, Migrieren von Untertiteln
- Synchronisierter, barrierefreier Medienaustausch (Sami), Migrieren von Untertiteln
- Sami (synchronisierter, barrierefreier Medienaustausch), Migrieren von Untertiteln
- Migrations Handbuch, synchronisierter zugänglicher Medienaustausch (Sami)
- Migrations Handbuch, Untertitel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101306"
---
# <a name="closed-captioning"></a>Untertitel

Das ActiveX-Steuerelement von Windows Media Player 6,4 enthält einen integrierten Untertitel für die Untertitelanzeige, der bei sichtbar gemachten Untertiteln für den geschlossenen, zugänglichen Medienaustausch (Sami) aktiviert und den Text der geschlossenen Überschrift anzeigt. Das Steuerelement Windows Media Player 7 oder höher ermöglicht die Anzeige von Sami Closed Caption mithilfe eines HTML- **<DIV>** Elements. Beispiel:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Diese Technik bietet Ihnen vollständige Flexibilität, da Sie Ihre Webseite so entwerfen können, dass Untertitel auf angepasste Weise angezeigt werden. die Anzeige der geschlossenen Beschriftung ist nicht mehr erforderlich, um an einem bestimmten Speicherort neben der Windows Media Player-Benutzeroberfläche zu liegen.

Nachdem Sie einen Bereich zum Anzeigen von Untertiteln erstellt haben, verwenden Sie *closedcaption*. **captioningid** -Eigenschaft, um den Speicherort anzugeben, an dem Windows Media Player den geschlossenen Beschriftungs Text rendert.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Das Windows Media Player Software Development Kit (SDK) enthält ein funktionierendes Beispiel eines eingebetteten Players, der einen geschlossenen Beschriftungs Text anzeigt. Um die SDK-Beispiele zu erhalten, laden Sie das komplette Windows Media Player SDK von der Microsoft-Website herunter, und installieren Sie es. Weitere Informationen zu geschlossenen Beschriftungen und Sami finden Sie auf der [Microsoft-Website für Barrierefreiheit](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> </dl>

 

 




