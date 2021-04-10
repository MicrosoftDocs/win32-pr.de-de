---
description: Die dvdadm. bookmarkonstoppt-Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der dem mswebdvd-Objekt mitteilt, ob ein Lesezeichen des aktuellen Speicher Orts und der Einstellungen automatisch gespeichert werden soll, wenn der Benutzer auf die Schaltfläche Beenden klickt.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Bookmarkonstoppt (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125054"
---
# <a name="bookmarkonstop-property"></a>Bookmarkonstoppt (Eigenschaft)

Die- `DVDAdm.BookmarkOnStop` Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der das mswebdvd-Objekt anweist, ob ein Lesezeichen des aktuellen Speicher Orts und **der** Einstellungen automatisch gespeichert werden soll, wenn der Benutzer auf die Schaltfläche

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob das msdvdadm-Objekt ein Lesezeichen aller DVD-Einstellungen speichert, einschließlich der Position auf der Festplatte, der Jugendebene und dem Eltern Land/der Region

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.

Lesezeichen sind nur für einen bestimmten Computer gültig. Ein Benutzer kann ein Lesezeichen nicht speichern und dann an eine andere Person senden, um Sie auf einem anderen Computer zu lesen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bookmarkonclose**](bookmarkonclose-property.md)
</dt> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



