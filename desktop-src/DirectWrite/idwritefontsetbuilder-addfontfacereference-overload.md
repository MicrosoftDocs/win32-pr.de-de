---
title: IDWriteFontSetBuilder AddFontFaceReference-Methoden (Dwrite \_ 3.h)
description: Fügt der gruppe, die erstellt wird, einen Verweis auf eine Schriftart hinzu.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- AddFontFaceReference-Methoden Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c9edfed7680b18ef9ffb271cb59de3a54d4b408ac5f194a7bead1bbb3fb9b2ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075580"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>IDWriteFontSetBuilder::AddFontFaceReference-Methoden

Fügt der gruppe, die erstellt wird, einen Verweis auf eine Schriftart hinzu.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference(IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Fügt der gruppe, die erstellt wird, einen Verweis auf eine Schriftart hinzu. Die erforderlichen Metadaten werden automatisch aus der Schriftart extrahiert, wenn CreateFontSet aufgerufen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference(IDWriteFontFaceReference \* , const DWRITE \_ FONT \_ PROPERTY \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Fügt der gruppe, die erstellt wird, einen Verweis auf eine Schriftart hinzu. Der Aufrufer stellt genügend Informationen für die Suche bereit, um zu vermeiden, dass die potenziell nicht lokale Schriftart geöffnet werden muss. Alle Eigenschaften, die nicht vom Aufrufer bereitgestellt werden, fehlen, und diese Eigenschaften sind in GetMatchingFonts nicht als Filter verfügbar. GetPropertyValues für fehlende Eigenschaften gibt eine leere Zeichenfolgenliste zurück. Die übergebenen Eigenschaften sollten im Allgemeinen mit dem tatsächlichen Schriftartinhalt konsistent sein, müssen jedoch nicht übereinstimmen. Sie können z. B. einen Alias für eine Schriftart mit einem anderen Namen oder eindeutigen Bezeichner verwenden oder benutzerdefinierte Tags festlegen, die in der tatsächlichen Schriftart nicht vorhanden sind.<br/> |



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
