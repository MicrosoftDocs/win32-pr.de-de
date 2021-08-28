---
title: Klassen und Server
description: Klassen und Server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b87ce6b52e73f8ac4e465202b787a2c65dc563f3d7c0678ef82b91601351d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993800"
---
# <a name="classes-and-servers"></a>Klassen und Server

COM verwendet **HKEY \_ CLASSES \_ ROOT** für computerweite Einstellungen, ermöglicht aber auch die benutzerspezifische Konfiguration von CLSIDS für mehr Sicherheit und Flexibilität. COM verwendet zuerst **HKEY \_ CURRENT USER \_ Software \\ \\ Classes,** bevor unter **HKEY CLASSES ROOT nach gesucht \_ \_ wird.** COM speichert computerweite Informationen zu CLSIDs unter **HKEY \_ CLASSES ROOT \_ \\ CLSID** und benutzerspezifische Klasseninformationen unter **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID.**

COM-Server unterstützen die Selbstregistrierung. Für einen Prozessserver bedeutet dies, dass die DLL die folgenden Funktionen exportieren muss:

-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Sie müssen diese Funktionen explizit exportieren, indem Sie eine Moduldefinitionsdatei, Linkerschalter oder Compiler-Direktiven verwenden. Der Klassenspeicher verwendet diese Funktionen, um die lokale Registrierung zu konfigurieren, nachdem die Datei auf den Clientcomputer heruntergeladen wurde. Zusätzlich zum Klassenspeicher werden diese Funktionen auch von anderen Umgebungen verwendet, um Server auf Hostcomputern zu installieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 