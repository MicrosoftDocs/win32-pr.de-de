---
title: Idwrite-fontsetbuilder addfontfacereferenzierungsmethoden (dwrite \_ 3. h)
description: Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Addfontfacereferenzierungsmethoden direkt schreiben
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372155"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>Idwrite-fontsetbuilder:: addfontfacereferenzierungsmethoden

Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addfontfakereferenzierung (idschreitefontfakereferenzierung \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu. Die erforderlichen Metadaten werden automatisch aus der Schriftart extrahiert, wenn createfontset aufgerufen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Addfontfakereferenzierung (idschreitefontfakereferenzierung \* , Konstante dwrite- \_ Schriftart \_ Eigenschaft \* , UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu. Der Aufrufer liefert genug Informationen, um zu suchen, und es wird vermieden, dass die möglicherweise nicht lokale Schriftart geöffnet werden muss. Alle Eigenschaften, die nicht vom Aufrufer bereitgestellt werden, fehlen, und diese Eigenschaften sind nicht als Filter in getmatchingfonts verfügbar. GetPropertyValues für fehlende Eigenschaften gibt eine leere Zeichen folgen Liste zurück. Die übergebenen Eigenschaften sollten im Allgemeinen mit dem tatsächlichen Schriftart Inhalt konsistent sein, Sie müssen jedoch nicht sein. Sie könnten z. b. eine Schriftart mit einem anderen Namen oder eindeutigen Bezeichner als Alias verwenden, oder Sie können benutzerdefinierte Tags festlegen, die nicht in der eigentlichen Schriftart vorhanden sind.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontsetbuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
