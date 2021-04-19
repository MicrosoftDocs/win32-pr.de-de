---
description: Die Klasse MSFT \_ Providers und die WMI-Fehler Behebungs Klassen sind eine Gruppe der MSFT-Ereignis Klassen, die mit WMI-Anbieter Ereignissen gekoppelt sind.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Anbieter Konfiguration und Fehler Behebungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349458"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Anbieter Konfiguration und Fehler Behebungs Klassen

Die Klasse [**MSFT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) und die WMI-Fehler Behebungs Klassen sind eine Gruppe der [MSFT-Ereignis Klassen](msft-classes.md) , die mit WMI-Anbieter Ereignissen gekoppelt sind.

Die Klasse der [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) enthält Konfigurationsinformationen für Anbieter und umfasst die folgenden Methoden, die es Ihnen ermöglichen, Anbieter zu laden und zu entladen oder Anbieter Vorgänge anzuhalten und fortzusetzen:

-   [**Load-Methode der Klasse der MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Entlade Methode der Klasse der MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Resume-Methode der Klasse der MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Suspend-Methode der Klasse der MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Die [WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md) werden benannt, um anzugeben, ob das Ereignis vor oder nach einem Anbieter Ereignis ausgelöst wird. Beispielsweise wird das Objekt " [**MSFT \_ WMIProvider \_ Access Check \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) " unmittelbar vor dem Aufruf der Implementierung von **iwbemeventsecurity:: AccessCheck** des Anbieters generiert, während das Objekt " [**MSFT \_ WMIProvider \_ AccessCheck \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) " unmittelbar nach aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
