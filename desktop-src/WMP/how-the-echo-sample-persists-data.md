---
title: Beibehalten von Daten durch das Echobeispiel
description: Beibehalten von Daten durch das Echobeispiel
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Windows Media Player-Plug-Ins, Echo-Beispieleigenschaftenseiten
- Plug-Ins, Echo-Beispieleigenschaftenseiten
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispieleigenschaftenseiten
- DSP-Plug-Ins, Echo-Beispieleigenschaftenseiten
- Echo-DSP-Plug-In-Beispiel, Eigenschaftenseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f725ef92134a634f805ce9ad713c9cf73825de44a26ace3f53b97bfd0efba63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837193"
---
# <a name="how-the-echo-sample-persists-data"></a>Beibehalten von Daten durch das Echobeispiel

Wenn Windows Media Player ein DSP-Plug-In aktiviert, können viele Instanzen des Plug-In-Objekts während einer Sitzung erstellt und zerstört werden. Das Plug-In benötigt eine Möglichkeit, seine Eigenschaftswerte zwischen Instanzen zu speichern. Der vom Windows Media Player Plug-In-Assistent generierte Beispielcode speichert diese Werte in der Registrierung und ruft sie ab, wenn die Eigenschaftenseite aufgerufen oder eine neue Instanz des Plug-Ins erstellt wird.

Der Standardbeispielcode in Echo.h enthält zwei Konstanten, die den Standardregistrierungspfad und die Skalierungsfaktor-Namenszeichenfolge speichern. Sie sollten die Variable beibehalten, die den Pfad angibt, aber die Zeile löschen, die den Namen der Skalierungsfaktorregistrierung angibt. Fügen Sie dann den folgenden Code hinzu, um Konstanten für die Verzögerungszeit und die Namen der Vermischungseigenschaften in der Registrierung zu definieren. Der fertige Abschnitt sollte wie folgt aussehen:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Sie verwenden diese Konstanten, wenn Sie die Methoden der Eigenschaftenseite ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Echo-Beispieleigenschaftenseite**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




