---
title: Idwrite-FONTSET GetPropertyValues-Methoden (dwrite \_ 3. h)
description: Gibt Eigenschaftswerte für den Schriftart Satz zurück.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- GetPropertyValues-Methoden direktes Schreiben
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354176"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Idwrite Test FONTSET:: GetPropertyValues-Methoden

Gibt Eigenschaftswerte für den Schriftart Satz zurück.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues (Eigenschaften-ID der dwrite- \_ Schriftart \_ \_ , idschreitestringlist \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familien Liste oder Tag Cloud verwendet werden können. Alle Werte werden unabhängig von der Sprache zurückgegeben, einschließlich aller lokalisierten Namen. <br/>                                                                                       |
| [**GetPropertyValues (Eigenschaften-ID der dwrite- \_ Schriftart \_ , Konstante \_ WCHAR \* , idschreitestringlist \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familien Liste oder Tag Cloud verwendet werden können. Werte werden in der Reihenfolge ihrer Priorität entsprechend der Sprachliste zurückgegeben. Wenn eine Schriftart mehr als einen lokalisierten Namen enthält, wird der bevorzugte Wert zurückgegeben. <br/> |
| [**GetPropertyValues (UInt32, dwrite \_ Font \_ Property \_ ID, bool \* , idschreitelocalizedstrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Gibt die Eigenschaftswerte eines bestimmten Schriftart Element Indexes zurück.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontset**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
