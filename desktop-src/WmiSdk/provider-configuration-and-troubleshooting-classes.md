---
description: Die MSFT \_ Providers-Klasse und die WMI-Problembehandlungsklassen sind eine Gruppe der MSFT-Ereignisklassen, die an WMI-Anbieterereignisse gekoppelt sind.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Anbieterkonfigurations- und Problembehandlungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d37443047e9bbde709fc1c7367f0691d16215eff62e39196987b466aea0830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050498"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Anbieterkonfigurations- und Problembehandlungsklassen

Die [**MSFT \_ Providers-Klasse**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) und die WMI-Problembehandlungsklassen sind eine Gruppe der [MSFT-Ereignisklassen,](msft-classes.md) die an WMI-Anbieterereignisse gekoppelt sind.

Die [**\_ MSFT-Anbieterklasse**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) enthält Konfigurationsinformationen für Anbieter und umfasst die folgenden Methoden, mit denen Sie Anbieter laden und entladen oder Anbietervorgänge aussetzen und fortsetzen können:

-   [**Load-Methode der \_ MSFT-Anbieterklasse**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**UnLoad-Methode der \_ MSFT-Anbieterklasse**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Resume-Methode der \_ MSFT-Anbieterklasse**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Suspend-Methode der \_ MSFT-Anbieterklasse**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Die [WMI-Problembehandlungsklassen](wmi-troubleshooting-classes.md) werden benannt, um anzugeben, ob das Ereignis vor oder nach einem Anbieterereignis ausgelöst wird. Beispielsweise wird das [**\_ \_ AccessCheck \_ Pre-Objekt von MSFT WmiProvider**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) unmittelbar vor dem Aufruf der Implementierung von **IWbemEventSecurity::AccessCheck** des Anbieters generiert, während das [**\_ \_ AccessCheck \_ Post-Objekt von MSFT WmiProvider**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) unmittelbar danach aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei WMI](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Problembehandlungsklassen](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
