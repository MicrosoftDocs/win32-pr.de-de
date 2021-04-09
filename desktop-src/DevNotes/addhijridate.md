---
description: HKCU- \\ Systemsteuerung \\ International.
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: Addhijridate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860808"
---
# <a name="addhijridate"></a>Addhijridate

**HKCU- \\ Systemsteuerung \\ International**



| Datentyp | Range                      | Standardwert |
|-----------|----------------------------|---------------|
| REG- \_ SZ   | *Ein gültiger Anpassungswert* | (Keine)        |



 

## <a name="description"></a>BESCHREIBUNG

Gibt Anpassungen für das Datum innerhalb des Hijri-Kalenders an.

Der Hijri-Kalender ist ein Mondkalender, der in der islamischen Welt verwendet wird. Die Monate beginnen und enden gemäß einem Dekret, das auf der Beobachtung des neuen Mond basiert. Es ist schwierig, den Beginn und die Enden der Monate genau vorherzusagen, und es gibt regionale Variationen, sodass zwischen 0 und zwei Tagen eine Anpassung an den Kalender erfolgt.

Der Registrierungs Wert **addhijridate** speichert diesen Anpassungswert wie folgt.



| Wert          | Bedeutung                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Addhijridate-2 | Subtrahieren Sie zwei Tage.                                                                                                                                                                                                                    |
| Addhijridate   | Subtrahieren Sie einen Tag.                                                                                                                                                                                                                     |
| (leer)        | Es ist keine Anpassung erforderlich. (Wenn das Datum nicht angepasst wurde, wird dieser Eintrag nicht in der Registrierung angezeigt. Wenn das Datum angepasst und dann auf den ursprünglichen Wert wieder hergestellt wurde, wird dieser Eintrag in der Registrierung ohne Wert angezeigt.) |
| Addhijridate + 1 | Fügen Sie einen Tag hinzu.                                                                                                                                                                                                                          |
| Addhijridate + 2 | Fügen Sie zwei Tage hinzu.                                                                                                                                                                                                                         |



 

Dieser Eintrag ist nicht standardmäßig in der Registrierung vorhanden. Sie können ihn mithilfe des Registrierungs-Editors Regedit.exe oder mithilfe der unten beschriebenen Änderungs Methode hinzufügen.

## <a name="change-method"></a>Methode ändern

Um den Wert dieses Eintrags zu ändern oder ihn der Registrierung hinzuzufügen, installieren Sie zunächst die Dateien für das komplexe Skript und die Sprachen von rechts nach links. Klicken Sie in der Systemsteuerung auf Regions **-und Sprachoptionen, und** klicken Sie dann auf die Registerkarte **Sprachen** . Aktivieren Sie unter **zusätzliche Sprachunterstützung** das Kontrollkästchen zum **Installieren von Dateien für komplexe Skripts und Sprachen von rechts nach links (einschließlich Thai)**. Klicken Sie auf **OK**.

Um den Wert dieses Eintrags zu ändern oder ihn der Registrierung hinzuzufügen, klicken Sie in der Systemsteuerung auf Regions **-und Sprachoptionen**. Wählen Sie im Feld **Standards und Formate** ein Gebiets Schema aus, das den Hijri-Kalender verwendet. Klicken Sie auf die Schaltfläche **Anpassen** und dann auf die Registerkarte **Datum** . Wählen Sie in der Dropdown Liste **Hijri-Datum anpassen an:** den entsprechenden Wert aus. Klicken Sie auf **OK** und dann erneut auf **OK** .

## <a name="activation-method"></a>Aktivierungsmethoden

Änderungen an diesem Eintrag, die über die Systemsteuerung vorgenommen werden, treten sofort in Kraft.

 

 



