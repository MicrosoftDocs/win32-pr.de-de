---
description: HKCU \\ Systemsteuerung \\ International.
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00315b66b53960ae392f8b0daf8f23f3c81302c5adcc4314bf982f85c8dc2bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390730"
---
# <a name="addhijridate"></a>AddHijriDate

**HKCU \\ Systemsteuerung \\ International**



| Datentyp | Range                      | Standardwert |
|-----------|----------------------------|---------------|
| REG \_ SZ   | *Ein gültiger Anpassungswert* | (Keine)        |



 

## <a name="description"></a>BESCHREIBUNG

Gibt Anpassungen am Datum im Hijri-Kalender an.

Der Hijri-Kalender ist ein Mondkalender, der in der Welt der Mondlande verwendet wird. Die Monate beginnen und enden gemäß einer Ante, die auf der Beobachtung des neuen Mondes basiert. Es ist schwierig, die Anfangs- und Endzeiten der Monate genau vorherzusagen, und es gibt regionale Variationen, sodass eine Anpassung zwischen 0 und zwei Tagen an den Kalender vorgenommen wird.

Der Registrierungswert **AddHijriDate** speichert diesen Anpassungswert wie folgt.



| Wert          | Bedeutung                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHijriDate-2 | Subtrahieren Sie zwei Tage.                                                                                                                                                                                                                    |
| AddHijriDate   | Subtrahieren Sie einen Tag.                                                                                                                                                                                                                     |
| (leer)        | Es ist keine Anpassung erforderlich. (Wenn das Datum nicht angepasst wurde, wird dieser Eintrag nicht in der Registrierung angezeigt. Wenn das Datum angepasst und dann auf den ursprünglichen Wert wiederhergestellt wurde, wird dieser Eintrag in der Registrierung ohne Wert angezeigt.) |
| AddHijriDate+1 | Fügen Sie einen Tag hinzu.                                                                                                                                                                                                                          |
| AddHijriDate+2 | Fügen Sie zwei Tage hinzu.                                                                                                                                                                                                                         |



 

Dieser Eintrag ist nicht standardmäßig in der Registrierung vorhanden. Sie können sie mithilfe des Registrierungs-Editors Regedit.exe oder mithilfe der unten beschriebenen Änderungsmethode hinzufügen.

## <a name="change-method"></a>Methode ändern

Um den Wert dieses Eintrags zu ändern oder zur Registrierung hinzuzufügen, installieren Sie zunächst die Dateien für komplexe Skripts und Sprachen von rechts nach links. Klicken Sie in Systemsteuerung auf **Regions- und Sprachoptionen** und dann auf die Registerkarte **Sprachen.** Aktivieren Sie unter **Ergänzende Sprachunterstützung** das Kontrollkästchen Dateien für komplexe Skripts und Sprachen von **rechts nach links installieren (einschließlich Thailändisch).** Klicken Sie auf **OK**.

Um den Wert dieses Eintrags zu ändern oder ihn der Registrierung hinzuzufügen, klicken Sie Systemsteuerung auf **Regionale optionen und Sprachoptionen**. Wählen Sie im Feld **Standards und Formate** ein Gebietsschema aus, das den Hijri-Kalender verwendet. Klicken Sie auf die Schaltfläche **Anpassen** und dann auf die Registerkarte **Datum.** Wählen Sie in der Dropdownliste **Hijri date to: (Hijri-Datum an: anpassen)** den entsprechenden Wert aus. Klicken Sie auf **OK** und dann erneut auf **OK.**

## <a name="activation-method"></a>Aktivierungsmethoden

Änderungen an diesem Eintrag, die über Systemsteuerung vorgenommen wurden, werden sofort wirksam.

 

 



