---
description: Die currentsubpicturestream-Eigenschaft legt den aktuellen teilbildstream fest oder ruft ihn ab.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Currentsubpicturestream (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522568"
---
# <a name="currentsubpicturestream-property"></a>Currentsubpicturestream (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `CurrentSubpictureStream` Eigenschaft legt den aktuellen teilbildstream fest oder ruft ihn ab.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Integer-Wert zurück, der den Stream darstellt.

## <a name="remarks"></a>Bemerkungen

Mögliche Werte für diese Eigenschaft:



| Wert   | BESCHREIBUNG              |
|---------|--------------------------|
| 0 bis 31 | Der teilbildstream    |
| 63      | Gedämpfter Datenstrom mit niedriger Bitrate |



 

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Bevor Sie einen neuen teilbildstream festlegen, wenden Sie [**issubpicturestreamaktivian**](issubpicturestreamenabled-method.md) , um zu überprüfen, ob der Stream verfügbar ist.

Das Festlegen dieser Eigenschaft bewirkt, dass die Eigenschaft " [**subpictureon**](subpictureon-property.md) " in " **true**" gewechselt wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Subpictureon**](subpictureon-property.md)
</dt> <dt>

[**Subpicturestreamsavailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



