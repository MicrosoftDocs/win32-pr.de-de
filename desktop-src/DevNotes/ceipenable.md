---
description: HKLM \\ Software \\ Microsoft \\ SQMClient Windows \\ \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687e17bf5438406fb7a29b954bf8a2640fc0ea5d193ba49ae7fd7bd02f1f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956119"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient Windows \\ \\ CEIPEnable**



| Datentyp  | Range                     | Standardwert |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (deaktivieren) oder 1 (aktivieren) | 0             |



 

## <a name="description"></a>Beschreibung

Aktiviert das Windows Programm zur Verbesserung der Benutzererfahrung.

## <a name="change-method"></a>Methode ändern

Um den Wert dieses Eintrags zu ändern, wählen Sie in Systemsteuerung System und **Wartung** aus, gefolgt von **Problemberichten und Lösungen**. Klicken **Sie im Abschnitt Einstellungen** auf Verbesserung der Benutzererfahrung.

## <a name="activation-method"></a>Aktivierungsmethoden

An diesem Eintrag vorgenommene Änderungen werden sofort wirksam. Wenn Sie diesen Registrierungsschlüssel aktivieren, wird Windows Programm zur Verbesserung der Benutzerfreundlichkeit für den gesamten Computer aktiviert. Wenn Sie diesen Registrierungsschlüssel deaktivieren, wird Windows Programm zur Verbesserung der Benutzerfreundlichkeit für den gesamten Computer deaktiviert.

Dieser Eintrag kann durch eine Einstellung für Gruppenrichtlinie auf Systemen ersetzt werden, die Gruppenrichtlinie. Während die Windows Programm zur Verbesserung der Benutzerfreundlichkeit CEIP enable Gruppenrichtlinie aktiviert ist, ignoriert das System diesen Eintrag. Die Konfiguration dieser Richtlinieneinstellung wird  im Abschnitt Richtlinien unter **HKLM \\ Software Policies Microsoft \\ \\ \\ SQMClient Windows \\ \\ CEIPEnable gespeichert.**

 

 



