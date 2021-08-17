---
description: Speichern und Wiederherstellen von DvdState-Objekten
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Speichern und Wiederherstellen von DvdState-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922851cce72f736364c1f1e66b24032586221ad9cb75494c7286fe962eb34403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982570"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Speichern und Wiederherstellen von DvdState-Objekten

[**IDvdState-Objekte**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) ermöglichen Es Anwendungen, eine Momentaufnahme der Benutzersitzung zu speichern, einschließlich Informationen wie dem aktuellen Speicherort auf dem Datenträger, der Elternebene der Person, die angezeigt wird, den ausgewählten Audio- und Bilddatenströmen usw. Dies bedeutet, dass Benutzer ihre Position auf einem DVD-Video Datenträger speichern und zu einem späteren Zeitpunkt ansehen können.

Anwendungen können keine DvdState-Objekte erstellen. Diese Objekte werden intern vom DVD-Navigator erstellt, wenn eine Anwendung [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate)aufruft. DvdState-Objekte machen die [**IDvdState-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) verfügbar, damit Anwendungen bestimmte Informationen abfragen können.

In der DVD-Beispielanwendung zeigen die Funktionen **CDvdCore::RestoreBookmark** und **CDvdCore::SaveBookmark,** wie DvdState-Objekte gespeichert und abgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



