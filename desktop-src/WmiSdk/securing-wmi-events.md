---
description: WMI-Ereignisse werden vom Ereignis Anbieter an einen temporären oder permanenten Consumer übermittelt. Das WMI-Ereignis System verwendet den Vergleich der Sicherheits Deskriptoren für Ereignisse und Benutzerkonten-SIDs, um den Zugriff auf das Ereignis zu steuern.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Sichern von WMI-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215327"
---
# <a name="securing-wmi-events"></a>Sichern von WMI-Ereignissen

WMI-Ereignisse werden vom [*Ereignis Anbieter*](gloss-e.md) an einen [*temporären*](gloss-t.md) oder [*permanenten*](gloss-p.md) Consumer übermittelt. Das WMI-Ereignis System verwendet den Vergleich der [*Sicherheits Deskriptoren*](gloss-s.md) für Ereignisse und Benutzerkonten- [*SIDs*](gloss-s.md) , um den Zugriff auf das Ereignis zu steuern.

Ereignisse werden normalerweise in Form einer Instanz einer Ereignisklasse übermittelt, aber nicht notwendigerweise vom [**\_ \_ Ereignis**](--event.md)abgeleitet. WMI bietet mehrere allgemeine Ereignis Klassen in den [WMI-System Klassen](wmi-system-classes.md), z. b. [**\_ \_ instancemodificationevent**](--instancemodificationevent.md). Anbieter können auch Ihre eigenen Ereignis Klassen angeben. Der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) verfügt z. b. über Ereignis Klassen, die die Änderung eines Registrierungsschlüssels oder-Werts melden, z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

In den folgenden Themen finden Sie Informationen zur sicheren Übermittlung von Ereignissen für Anbieter und zum sicheren empfangen von Ereignissen für Client Skripts und Anwendungen:

-   [Sicheres Bereitstellen von Ereignissen](providing-events-securely.md)
-   [Sicheres empfangen von Ereignissen](receiving-events-securely.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

 
