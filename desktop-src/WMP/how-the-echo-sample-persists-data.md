---
title: So speichert das Echo Beispiel Daten
description: So speichert das Echo Beispiel Daten
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711561"
---
# <a name="how-the-echo-sample-persists-data"></a>So speichert das Echo Beispiel Daten

Wenn Windows Media Player ein DSP-Plug-in aktiviert, kann es während einer Sitzung viele Instanzen des Plug-in-Objekts erstellen und zerstören. Das Plug-in benötigt eine Möglichkeit, seine Eigenschaftswerte zwischen Instanzen beizubehalten. Der Beispielcode, der vom Assistenten für Windows-Media Player-Plug-ins generiert wird, speichert diese Werte in der Registrierung und ruft Sie ab, wenn die Eigenschaften Seite aufgerufen wird oder wenn eine neue Instanz des Plug-Ins erstellt wird.

Der Standardbeispiel Code in Echo. h enthält zwei Konstanten, die den Standard Registrierungs Pfad und die Name-Zeichenfolge des Skalierungsfaktors speichern. Behalten Sie die Variable bei, die den Pfad angibt, aber löschen Sie die Zeile, in der der Registrierungs Name des Skalierungsfaktors angegeben ist. Fügen Sie anschließend den folgenden Code hinzu, um Konstanten für die Verzögerungszeit-und nass Mischungs Eigenschaftsnamen in der Registrierung zu definieren. Der fertige Abschnitt sollte wie folgt aussehen:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Diese Konstanten werden verwendet, wenn Sie die Methoden der Eigenschaften Seite ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




