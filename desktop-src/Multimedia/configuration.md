---
title: Konfiguration (Windows Multimedia)
description: Erfahren Sie, wie Ein Windows Multimedia-Treiber Benutzern das Auswählen von Konfigurationseinstellungen ermöglichen kann, indem ein Konfigurationsdialogfeld angezeigt wird.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- Installierbare Treiber, Konfiguration
- Installierbare Treiber, DRV_CONFIGURE Meldung
- DRV_CONFIGURE Meldung
- DRV_QUERYCONFIGURE Meldung
- DRVCONFIGINFO-Meldung
- Konfigurieren von installierbaren Treibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403923"
---
# <a name="configuration-windows-multimedia"></a>Konfiguration (Windows Multimedia)

Mit einem installierbaren Treiber können Benutzer Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen, indem sie bei der Verarbeitung der [**DRV \_ CONFIGURE-Meldung**](drv-configure.md) ein Konfigurationsdialogfeld anzeigen. Der Treiber ist dafür verantwortlich, das Dialogfeld zu erstellen und zu verwalten, alle Benutzereingaben aus dem Dialogfeld zu verarbeiten und die Konfiguration des Treibers oder der Hardware wie vom Benutzer angefordert zu ändern. Der Treiber muss eine separate Dialogfeldprozedur zum Verarbeiten von Fenstermeldungen für das Dialogfeld und eine Dialogfeldvorlage bereitstellen, um die Darstellung und den Inhalt des Dialogfelds zu definieren.

Vor dem Empfang der DRV \_ CONFIGURE-Nachricht empfängt ein Treiber die [**DRV \_ QUERYCONFIGURE-Nachricht.**](drv-queryconfigure.md) Der Treiber muss einen Wert ungleich 0 (null) an die Abfrage zurückgeben, um sicherzustellen, dass die nachfolgende DRV \_ CONFIGURE-Nachricht empfangen wird.

Beim Initialisieren des Konfigurationsdialogfelds ruft der Treiber in der Regel Konfigurationsinformationen aus der Registrierung ab. Um diese Informationen zu finden, enthält die DRV \_ CONFIGURE-Nachricht in der Regel die Adresse einer [**DRVCONFIGINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) die die Namen des Registrierungsschlüssels und den wert enthält, der dem Treiber zugeordnet ist. Wenn der Benutzer Änderungen an der Konfiguration anfordert, sollte der Treiber die Konfigurationsinformationen in der Registrierung aktualisieren.

 

 
