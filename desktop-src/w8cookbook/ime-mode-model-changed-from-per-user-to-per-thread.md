---
title: IME-modusmodelländerungen
description: IME-modusmodell von pro Benutzer in Thread pro Thread geändert
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316155"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>IME-modusmodell von pro Benutzer in Thread pro Thread geändert

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

In Windows 8 basieren der IME-Konvertierungsmodus und der IME-Satz Modus auf dem Benutzer Kontext, und das Ändern des Modus einer Anwendung betraf alle anderen Anwendungen. Dieses Verhalten kann deaktiviert werden, indem Sie im Abschnitt "Erweiterte Einstellungen" der sprach Systemsteuerung die Einstellung "eine andere Eingabemethode für die einzelnen App-Fenster festlegen" verwenden.

Um die Kompatibilität zu verbessern, werden die Modi in Windows 8.1 in einem Eingabe Kontext gespeichert, unabhängig davon, wie das Steuerelement "legen Sie eine andere Eingabemethode für jedes App-Fenster festlegen" festgelegt wird. In Windows 8.1 wirkt sich die Einstellung "eine andere Eingabemethode für jedes App-Fenster festlegen" nur auf die Auswahl der Eingabemethode selbst aus.

Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:



|          | Software Eingabebereich | Hardware Tastatur |
|----------|----------------------|-------------------|
| Kor, jpn | Ein                   | Aus               |
| CHS, cht  | Ein                   | Ein                |



 

## <a name="manifestations"></a>Kundgebungen

Wenn ein Benutzer den IME-Modus für eine Anwendung ändert, wirkt sich die Änderung nicht auf andere Anwendungen aus.

## <a name="resources"></a>Ressourcen

-   [Werte des IME-Konvertierungsmodus](../intl/ime-conversion-mode-values.md)
-   [Werte für den IME-Satzmodus](../intl/ime-sentence-mode-values.md)

 

 