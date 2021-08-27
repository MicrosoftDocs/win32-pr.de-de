---
description: DMOEnum-Beispiel
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: DMOEnum-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fc51cc45ad879ccbc5ccd232b782e4b9f5511071d8d2492c135efcb322969c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079200"
---
# <a name="dmoenum-sample"></a>DMOEnum-Beispiel

## <a name="description"></a>BESCHREIBUNG

Diese Beispielanwendung listet alle [DirectX Media Objects](directx-media-objects.md) (DMOs) auf, die im System des Benutzers registriert sind, und zeigt Informationen darüber an.

Im Beispiel werden die [**DMOEnum-Funktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) und die [**IEnumDMO-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) zum Aufzählen der DMOs verwendet. Sie verwendet die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) und andere DMO Schnittstellen, um Informationen zu den einzelnen DMO.

## <a name="usage"></a>Verwendung

Wenn die Anwendung gestartet wird, werden alle installierten DMOs aufzählt. Wenn Sie eine bestimmte DMO auswählen, zeigt die Anwendung nur die DMOs in dieser Kategorie an. Um Informationen zu einem DMO, wählen Sie den DMO aus der Liste aus. Die Anwendung zeigt die Anzahl der Datenströme, die bevorzugten Medientypen, den DLL-Server für DMO und andere Informationen zum DMO. Um schlüsselierte DMOs ein- oder auszuschließen, aktivieren Sie das Kontrollkästchen **Include Keyed DMOs? (Schlüsselierte DMOs** enthalten?).

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* Samples Multimedia \\ \\ \\ DirectShow \\ Misc \\ DMOEnum.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



