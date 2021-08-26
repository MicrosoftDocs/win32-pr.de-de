---
description: Die DVDAdm.BookmarkOnClose-Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der das MSDVDAdm-Objekt darüber informiert, ob ein Lesezeichen des aktuellen Speicherorts und der aktuellen Einstellungen automatisch gespeichert werden soll, wenn der Benutzer die Anwendung schließt.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: BookmarkOnClose-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83ed0ef05e2efe7edb3b6494e8f9709b23259207af257957551077dfbbddaba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103340"
---
# <a name="bookmarkonclose-property"></a>BookmarkOnClose-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der das MSDVDAdm-Objekt darüber informiert, ob ein Lesezeichen des aktuellen Speicherorts und der aktuellen Einstellungen automatisch gespeichert werden soll, wenn der Benutzer die `DVDAdm.BookmarkOnClose` Anwendung schließt.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der bei "true" angibt, dass das MSDVDAdm-Steuerelement ein Lesezeichen aller DVD-Einstellungen einschließlich der Position auf dem Datenträger, der Elternebene und des Lands/der Region des Elternkontos gespeichert, wenn der Benutzer die DVD-Playeranwendung schließt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist mit dem Standardwert true gelesen/geschrieben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



