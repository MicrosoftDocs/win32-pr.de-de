---
description: Speichern und Wiederherstellen von dvdstate-Objekten
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Speichern und Wiederherstellen von dvdstate-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346595"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Speichern und Wiederherstellen von dvdstate-Objekten

[**Idvdstate**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) -Objekte ermöglichen es Anwendungen, eine Momentaufnahme der Benutzersitzung zu speichern, einschließlich Informationen wie dem aktuellen Speicherort auf der Festplatte, der Jugendebene der Person, die die Anzeige durchsucht, der ausgewählten Audiodaten und der teilbildstreams usw. Dies bedeutet, dass Benutzer ihren Speicherort auf einem DVD-Video-CD speichern und ihn zu einem späteren Zeitpunkt ansehen können.

Anwendungen können keine dvdstate-Objekte erstellen. Diese Objekte werden intern vom DVD-Navigator erstellt, wenn eine Anwendung [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate)aufruft. Dvdstate-Objekte machen die [**idvdstate**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) -Schnittstelle verfügbar, damit Anwendungen bestimmte Informationen Abfragen können.

In der DVD-Beispielanwendung zeigen die **cdvdcore:: restorebookmark** -und **cdvdcore:: savebookmark** -Funktionen, wie dvdstate-Objekte gespeichert und abgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



