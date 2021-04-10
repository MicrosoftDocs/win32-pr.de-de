---
description: Dmuerum-Beispiel
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Dmuerum-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213981"
---
# <a name="dmoenum-sample"></a>Dmuerum-Beispiel

## <a name="description"></a>BESCHREIBUNG

In dieser Beispielanwendung werden alle im System des Benutzers registrierten [DirectX Media Objects](directx-media-objects.md) (DMOs) aufgelistet, und es werden Informationen darüber angezeigt.

Im Beispiel werden die DMOS mithilfe der [**dmoenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion und der [**ienumdmo**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) -Schnittstelle aufgelistet. Er verwendet die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle und andere DMO-Schnittstellen zum Abrufen von Informationen zu jedem DMO.

## <a name="usage"></a>Verbrauch

Beim Starten der Anwendung werden alle installierten DMOS aufgelistet. Wenn Sie eine bestimmte DMO-Kategorie auswählen, werden in der Anwendung nur die DMOS in dieser Kategorie angezeigt. Wenn Sie Informationen zu einem DMO anzeigen möchten, wählen Sie in der Liste den DMO aus. Die Anwendung zeigt die Anzahl der Streams, die bevorzugten Medientypen, den DLL-Server für den DMO und weitere Informationen zum DMO an. Wenn Sie verschlüsselte DMOS einschließen oder ausschließen möchten, aktivieren Sie das Kontrollkästchen "Schlüssel **einschließen** ".

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ misc \\ dmuenum.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



