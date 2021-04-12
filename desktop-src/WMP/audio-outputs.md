---
title: Audioausgaben
description: Audioausgaben
ms.assetid: 2bedf804-c9fd-4a44-9289-e36a50517b7f
keywords:
- Windows Media Player, Audioausgaben
- Windows Media Player, DirectSound-Standardgerät
- Windows Media Player, econsole
- Windows Media Player, emultimedia
- Windows Media Player, eCommunications
- Audioausgaben
- DirectSound-Standardgerät
- econsole
- emultimedia
- eCommunications
- Windows Media Player ActiveX-Steuerelement, Audioausgaben
- Windows Media Player ActiveX-Steuerelement, DirectSound-Standardgerät
- Windows Media Player ActiveX-Steuerelement, econsole
- Windows Media Player ActiveX-Steuerelement, emultimedia
- Windows Media Player ActiveX-Steuerelement, eCommunications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb5ebefb3b2bb72e8314c843ce0fe7632f09652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388166"
---
# <a name="audio-outputs"></a>Audioausgaben

Die Systemsteuerung in Windows XP ermöglicht dem Benutzer das Zuweisen des Namens eines DirectSound-Standard Geräts zu einem bestimmten Audioausgabegerät. In Windows Vista kann der Benutzer in der Systemsteuerung jeden der drei Namen (econsole, emultimedia und eCommunications) einem Audioausgabegerät zuweisen. Diese Namen können jeweils unterschiedlichen Geräten zugewiesen werden, oder es können mehrere Namen demselben Gerät zugewiesen werden. Die folgende Tabelle zeigt, wie Windows Media Player und das Windows Media Player ActiveX-Steuerelement Standard-Audioausgabegeräte auswählen.



|                                      | Windows XP                                                                                                                                                                                | Windows Vista                                                                                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Player                 | Standardmäßig verwendet der Player das Audiogerät, das als DirectSound-Standardgerät festgelegt ist. Der Player stellt ein Dialogfeld bereit, mit dem der Benutzer den Player auf ein anderes Audiogerät umstellen kann. | Standardmäßig verwendet der Player das als emultimedia bezeichnete Audiogerät. Der Player stellt ein Dialogfeld bereit, mit dem der Benutzer den Player auf ein anderes Audiogerät umstellen kann. |
| Windows Media Player-ActiveX-Steuerelement | Standardmäßig verwendet das Player-Steuerelement das Audiogerät, das als DirectSound-Standardgerät festgelegt ist. Das Audioausgabegerät kann nicht Programm gesteuert geändert werden.                                | Standardmäßig verwendet das Player-Steuerelement das als emultimedia bezeichnete Audiogerät. Das Audioausgabegerät kann nicht Programm gesteuert geändert werden.                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




