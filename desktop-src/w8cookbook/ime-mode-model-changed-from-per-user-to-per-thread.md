---
title: Modelländerungen im IME-Modus
description: Das IME-Modusmodell wurde von "Pro Benutzer" in "Pro Thread" geändert.
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443247"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Das IME-Modusmodell wurde von "Pro Benutzer" in "Pro Thread" geändert.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

In Windows 8 basierten der IME-Konvertierungsmodus und der IME-Satzmodus auf dem Benutzerkontext, und das Ändern des Modus einer Anwendung hat sich auf alle anderen Anwendungen ausdrungen. Dieses Verhalten kann mithilfe der Einstellung "Let me set a different input method for each app window" im Abschnitt "Erweiterte Einstellungen" der Sprachsteuerung deaktiviert werden.

Zur Verbesserung der Kompatibilität werden die Modi in Windows 8.1 in einem Eingabekontext gespeichert, unabhängig davon, wie das Steuerelement "Let me set a different input method for each app window" festgelegt ist. In Windows 8.1 die Einstellung "Let me set a different input method for each app window" (Lass mich eine andere Eingabemethode für jedes App-Fenster festlegen) nur die Auswahl der Eingabemethode selbst.

Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:



| &nbsp;   | Softwareeingabebereich | Hardwaretastatur |
|----------|----------------------|-------------------|
| KOR, JPN | Ein                   | Aus               |
| CHS,CHT  | Ein                   | Ein                |



 

## <a name="manifestations"></a>Manifestationen

Wenn ein Benutzer den IME-Modus für eine Anwendung ändert, wirkt sich die Änderung nicht auf andere Anwendungen aus.

## <a name="resources"></a>Ressourcen

-   [Werte des IME-Konvertierungsmodus](../intl/ime-conversion-mode-values.md)
-   [IME-Satzmoduswerte](../intl/ime-sentence-mode-values.md)

 

 