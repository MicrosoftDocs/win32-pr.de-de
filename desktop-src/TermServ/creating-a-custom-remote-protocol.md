---
title: Erstellen eines Remotedesktopprotokoll Anbieters
description: Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters. Der Protokoll-Manager wird als COM-Server implementiert und an einem Ort registriert, der beim Starten des Remotedesktopdienste durchsucht wird.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a7905bfcc623174aca9152f0807a867112aee1a0c54976db810b87f8b3408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856216"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Erstellen eines Remotedesktopprotokoll Anbieters

Die folgenden Abschnitte enthalten Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters. Der Protokoll-Manager wird als COM-Server implementiert und an einem Ort registriert, der beim Starten des Remotedesktopdienste durchsucht wird.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Registrieren des Protokoll-Managers](registering-the-custom-protocol.md)
</dt> <dd>

Sie müssen mindestens einen Registrierungswerteintrag für Ihren Protokoll-Manager erstellen, damit Remotedesktopdienste Dienst ihn instanziieren kann.

</dd> <dt>

[Methodenaufrufsequenz](method-call-sequence.md)
</dt> <dd>

Der Remotedesktopdienste-Dienst und Ihr Protokollanbieter rufen sich gegenseitig in klar definierten Sequenzen auf.

</dd> </dl>

-   [Registrieren des Protokoll-Managers](registering-the-custom-protocol.md)
-   [Methodenaufrufsequenz](method-call-sequence.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopprotokoll-Anbieter-API](custom-remote-desktop-protocols.md)
</dt> <dt>

[Verwenden Remotedesktopdienste](using-terminal-services.md)
</dt> </dl>

 

 




