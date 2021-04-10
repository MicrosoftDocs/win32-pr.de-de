---
title: Konfiguration (Windows Multimedia)
description: Konfiguration
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- installierbare Treiber, Konfiguration
- installierbare Treiber, DRV_CONFIGURE Meldung
- DRV_CONFIGURE Meldung
- DRV_QUERYCONFIGURE Meldung
- Drvconfiginfo-Meldung
- Konfigurieren installier barer Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039962"
---
# <a name="configuration-windows-multimedia"></a>Konfiguration (Windows Multimedia)

Mithilfe eines installierbaren Treibers können Benutzer Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen, indem Sie beim verarbeiten [**der \_ drv**](drv-configure.md) -Konfigurations Nachricht ein Konfigurations Dialogfeld anzeigen. Der Treiber ist verantwortlich für das Erstellen und Verwalten des Dialog Felds, das Verarbeiten von Benutzereingaben aus dem Dialogfeld und das Ändern der Konfiguration des Treibers bzw. der Hardware, wie vom Benutzer angefordert. Der Treiber muss eine separate Dialogfeld Prozedur zum Verarbeiten von Fenster Meldungen für das Dialogfeld und eine Dialogfeld Vorlage bereitstellen, um die Darstellung und den Inhalt des Dialog Felds zu definieren.

Vor dem Empfang der drv- \_ Konfigurations Nachricht erhält ein Treiber die [**drv-Abfrage " \_ queryconfigure**](drv-queryconfigure.md) ". Der Treiber muss einen Wert ungleich 0 (null) an die Abfrage zurückgeben, um den Empfang der nachfolgenden drv- \_ Konfigurations Meldung sicherzustellen.

Wenn Sie das Dialogfeld Konfiguration initialisieren, ruft der Treiber normalerweise Konfigurationsinformationen aus der Registrierung ab. Um diese Informationen zu finden, enthält die drv \_ -Konfigurations Nachricht in der Regel die Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur, die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. Wenn der Benutzer Änderungen an der Konfiguration anfordert, sollte der Treiber die Konfigurationsinformationen in der Registrierung aktualisieren.

 

 
