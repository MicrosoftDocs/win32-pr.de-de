---
title: Unterschiedlichen Status Bits-Unterstützung
description: Unterschiedlichen Status Bits-Unterstützung
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036282"
---
# <a name="miscellaneous-status-bits-support"></a>Unterschiedlichen Status Bits-Unterstützung

ActiveX-Steuerelement Container müssen die folgenden OLEMISC-Status Bits erkennen und unterstützen \_ .



| Statusbit                           | Erforderlich?      | Kommentare                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Activateeinvisible<br/>       | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| Ignoreactivateeinvisible<br/> | Nein<br/>  | Erforderlich für die Unterstützung von inaktiven und fensterlosen Steuerelementen. Das ignoreactivateeinvisible-Bit ist für Container vorgesehen, die inaktive und fensterlose Steuerelemente Hosting. Das ignoreactivateeinvisible-Bit wird als Teil der ActiveX-Steuerelemente 96-Spezifikation eingeführt. Weitere Informationen finden Sie in dieser Dokumentation.<br/> |
| Insiout<br/>                 | Nein<br/>  | Wird in der Regel nicht mit ActiveX-Steuerelementen, sondern mit Verbund Dokument Einbettungen verwendet. Beachten Sie, dass dies eine SDK-Dokumentation ist, die besagt, dass dieses Bit festgelegt werden muss, damit das aktivierende activateeinsebit festgelegt wird<br/>                                                                             |
| Invisibleatruntime<br/>        | Ja<br/> | Bezeichnet ein Steuerelement, das zur Entwurfszeit sichtbar sein sollte, aber zur Laufzeit unsichtbar ist.<br/>                                                                                                                                                                                                       |
| Alwaysrun<br/>                 | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| Acsilikebutton<br/>            | Nein<br/>  | Die Unterstützung ist normalerweise obligatorisch, obwohl Sie für Container im Dokument Stil nicht erforderlich ist.<br/>                                                                                                                                                                                                    |
| Acsilikelabel<br/>             | Nein<br/>  | Die Unterstützung ist normalerweise obligatorisch, obwohl Sie für Container im Dokument Stil nicht erforderlich ist.<br/>                                                                                                                                                                                                    |
| Nomen aktivieren<br/>              | Ja<br/> |                                                                                                                                                                                                                                                                                                         |
| Alignable<br/>                 | Nein<br/>  |                                                                                                                                                                                                                                                                                                         |
| Simpleframe<br/>               | Nein<br/>  | Einschluss der [einfachen Frame Site](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| Zuerst SetClientSite<br/>        | Nein<br/>  | Die Unterstützung für dieses Bit wird empfohlen, ist jedoch nicht obligatorisch.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | Nein<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 





