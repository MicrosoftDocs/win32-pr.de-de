---
title: WM/Bild
description: Das WM/Bild-Attribut enthält ein Bild, das sich auf den Inhalt bezieht.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Bild Windows Media-Format
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948194"
---
# <a name="wmpicture"></a>WM/Bild

Das **WM/Bild-** Attribut enthält ein Bild, das sich auf den Inhalt bezieht.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmpicture

## <a name="data-type"></a>Datentyp

[**WM \_ Bild**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT \_ - \_ typbinär Datei**)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist mit dem ID3-Frame (APIC) kompatibel. Die ID3-Spezifikation für den APIC-Frame gibt an, dass es möglicherweise eine beliebige Anzahl von APIC-Frames gibt, die einer Datei zugeordnet sind, aber nur eine vom Typ "1" und nur eine vom Typ "2" sein kann. Die Spezifikation gibt auch an, dass die Beschreibung des Bilds nicht länger als 64 Zeichen sein kann, aber leer sein kann.

Die mit den Objekten des Windows Media SDK-SDKs hinzugefügten WM/Bild-Attribute werden nicht automatisch entsprechend den ID3-Spezifikationen überprüft. Sie müssen in Ihrer Anwendung Code hinzufügen, um Validierungen auszuführen, wenn Sie die vollständige Kompatibilität mit ID3 beibehalten möchten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM- \_ Bild**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




