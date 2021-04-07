---
title: Audioline-und Steuerelement Abfragen
description: Audioline-und Steuerelement Abfragen
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- Multimedia-Audiosteuer Elemente
- Audiodaten, Mixer-Steuerelemente
- Audiomixer, audiolinien
- audiolinien
- Audiomischungen, Steuerelemente
- Mischungen, Steuerelemente
- Mixer, audiolinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725088"
---
# <a name="audio-line-and-control-queries"></a>Audioline-und Steuerelement Abfragen

Die Mixer-Dienste stellen Funktionen zum Bestimmen von Informationen über audiolinien, audioliniensteuerelemente und Steuerelement Details bereit. Die Dienste stellen auch Funktionen zum Festlegen von Steuerungs Details bereit.

Sie können die [**mixergetlineinfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) -Funktion verwenden, um Informationen zu einer angegebenen audiozeile abzurufen. Diese Funktion füllt die [**mixerline**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) -Struktur für eine angegebene quellaudiozeile, eine zielaudiozeile oder einen Zeilen Bezeichner. Die Struktur enthält die Ziel Zeilennummer, die Anzahl der Kanäle in der Audiolinie sowie einen kurzen und langen Namen für die Audiolinie.

Die [**mixergetlinecontrols**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) -Funktion Ruft allgemeine Informationen zu einem oder mehreren Steuerelementen ab, die einer audiozeile zugeordnet sind. Diese Funktion füllt die [**mixerlinecontrols**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) -Struktur mit Informationen über das angegebene Steuerelement oder Steuerelemente aus. Sie können **mixergetlinecontrols** zum Abrufen von Steuerelement Eigenschaften für eine der folgenden Elemente verwenden:

-   Alle Steuerelemente für eine angegebene Quellzeile
-   Ein angegebenes Steuerelement für eine angegebene Quellzeile.
-   Das erste Steuerelement einer bestimmten Klasse für eine angegebene Quellzeile.

Die [**mixergetcontroldetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) -Funktion Ruft die Eigenschaften eines einzelnen Steuer Elements ab, das einer Audiolinie zugeordnet ist. Diese Funktion füllt die [**mixercontroldetails**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) -Struktur mit den aktuellen Werten für ein Steuerelement aus.

Die [**mixersetcontroldetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) -Funktion verwendet den Inhalt der **mixercontroldetails** -Struktur, um die Eigenschaften des angegebenen Steuer Elements festzulegen. Sie müssen sicherstellen, dass alle Elemente dieser Struktur ausgefüllt werden, bevor Sie **mixersetcontroldetails** aufrufen.

 

 