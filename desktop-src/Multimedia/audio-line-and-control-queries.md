---
title: Audiozeilen- und Steuerelementabfragen
description: Audiozeilen- und Steuerelementabfragen
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- Multimediaaudio, Mixer-Steuerelemente
- Audio, Mixer-Steuerelemente
- Audiomixer, Audiolinien
- Audiozeilen
- Audiomixer, Steuerelemente
- Mixer, Steuerelemente
- Mixer, Audiolinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c417b55273ba3f7f96cd857979c73003ed0f88c2161e1c2ac14d934fddcff1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692110"
---
# <a name="audio-line-and-control-queries"></a>Audiozeilen- und Steuerelementabfragen

Die Mixerdienste stellen Funktionen zum Bestimmen von Informationen zu Audiozeilen, Audiozeilensteuerelementen und Steuerelementdetails bereit. Die Dienste stellen auch Funktionen zum Festlegen von Steuerelementdetails bereit.

Sie können die [**mixerGetLineInfo-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) verwenden, um Informationen zu einer angegebenen Audiozeile abzurufen. Diese Funktion füllt die [**MIXERLINE-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) für eine angegebene Quellaudiozeile, Zielaudiozeile oder Zeilen-ID aus. Die Struktur enthält die Zielzeilennummer, die Anzahl der Kanäle in der Audiozeile sowie einen kurzen und einen langen Namen für die Audiozeile.

Die [**mixerGetLineControls-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) ruft allgemeine Informationen zu einem oder mehreren Steuerelementen ab, die einer Audiozeile zugeordnet sind. Diese Funktion füllt die [**MIXERLINECONTROLS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) mit Informationen über das angegebene Steuerelement oder die angegebenen Steuerelemente. Sie können **mixerGetLineControls** verwenden, um Steuerelementeigenschaften für eine der folgenden Eigenschaften abzurufen:

-   Alle Steuerelemente für eine angegebene Quellzeile
-   Ein angegebenes Steuerelement für eine angegebene Quellzeile
-   Das erste Steuerelement einer bestimmten Klasse für eine angegebene Quellzeile

Die [**mixerGetControlDetails-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) ruft Eigenschaften eines einzelnen Steuerelements ab, das einer Audiozeile zugeordnet ist. Diese Funktion füllt die [**MIXERCONTROLDETAILS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) mit den aktuellen Werten für ein Steuerelement.

Die [**mixerSetControlDetails-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) verwendet den Inhalt der **MIXERCONTROLDETAILS-Struktur,** um die Eigenschaften des angegebenen Steuerelements festzulegen. Sie müssen sicherstellen, dass alle Member dieser Struktur ausgefüllt sind, bevor Sie **mixerSetControlDetails** aufrufen.

 

 