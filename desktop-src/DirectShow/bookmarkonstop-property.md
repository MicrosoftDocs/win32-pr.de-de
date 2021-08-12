---
description: Die DVDAdm.BookmarkOnStop-Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der dem MSWebDVD-Objekt mitgibt, ob automatisch ein Lesezeichen des aktuellen Speicherorts und der Einstellungen gespeichert werden soll, wenn der Benutzer auf die Schaltfläche Beenden klickt.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: BookmarkOnStop-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73d8b9829075125437e05da96c78d101f5a7f5df4dc2decc25f044cc3f5f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662672"
---
# <a name="bookmarkonstop-property"></a>BookmarkOnStop-Eigenschaft

Die `DVDAdm.BookmarkOnStop` -Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der dem MSWebDVD-Objekt mitgibt, ob automatisch ein Lesezeichen des aktuellen Speicherorts und der Einstellungen gespeichert werden soll, wenn der Benutzer auf die Schaltfläche **Beenden** klickt.

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob das MSDVDAdm-Objekt ein Lesezeichen aller DVD-Einstellungen speichert, einschließlich der Position auf dem Datenträger, der Elternebene und des Lands/der Region der Eltern.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist lese-/schreibgeschützt und hat den Standardwert false.

Lesezeichen sind nur für einen bestimmten Computer gültig. Ein Benutzer kann ein Lesezeichen nicht speichern und dann an eine andere Person senden, um es auf einem anderen Computer zu lesen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



