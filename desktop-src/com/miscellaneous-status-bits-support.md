---
title: Unterstützung verschiedener Statusbits
description: Unterstützung verschiedener Statusbits
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096920"
---
# <a name="miscellaneous-status-bits-support"></a>Unterstützung verschiedener Statusbits

ActiveX Steuerelementcontainer müssen die folgenden OLEMISC-Statusbits erkennen und \_ unterstützen.



| Statusbit                           | Erforderlich?      | Kommentare                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | Nein<br/>  | Erforderlich für die Unterstützung von inaktiven und fensterlosen Steuerelementen. Das Bit IGNOREACTIVATEWHENVISIBLE ist für Container bestimmt, die inaktive und fensterlose Steuerelemente hosten. Das Bit IGNOREACTIVATEWHENVISIBLE wurde als Teil der spezifikation ActiveX Controls 96 eingeführt. Weitere Informationen finden Sie in dieser Dokumentation.<br/> |
| INSIDEOUT<br/>                 | Nein<br/>  | Wird nicht im Allgemeinen mit ActiveX-Steuerelementen verwendet, sondern mit zusammengesetzten Dokumenteinbettungen. Beachten Sie, dass dies im Gegensatz zu einer SDK-Dokumentation steht, die besagt, dass dieses Bit festgelegt werden muss, damit das ACTIVATEWHENVISIBLE-Bit festgelegt wird.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Ja<br/> | Legt ein Steuerelement fest, das zur Entwurfszeit, aber zur Laufzeit unsichtbar sein soll.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | Nein<br/>  | Die Unterstützung ist normalerweise obligatorisch, obwohl sie für Container im Dokumentstil nicht erforderlich ist.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | Nein<br/>  | Die Unterstützung ist normalerweise obligatorisch, obwohl sie für Container im Dokumentstil nicht erforderlich ist.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| Justierbar<br/>                 | Nein<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | Nein<br/>  | Siehe [Simple Frame Site Containment](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | Nein<br/>  | Unterstützung für dieses Bit wird empfohlen, ist aber nicht obligatorisch.<br/>                                                                                                                                                                                                                                       |
| Imemode<br/>                   | Nein<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 





