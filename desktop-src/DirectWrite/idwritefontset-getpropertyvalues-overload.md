---
title: IDWriteFontSet GetPropertyValues-Methoden (Dwrite \_ 3.h)
description: Gibt Eigenschaftswerte für den Schriftartensatz zurück.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- GetPropertyValues-Methoden – Direkter Schreibzugriff
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816361"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>IDWriteFontSet::GetPropertyValues-Methoden

Gibt Eigenschaftswerte für den Schriftartensatz zurück.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                   | Beschreibung                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familienliste oder tag cloud verwendet werden können. Alle Werte werden unabhängig von der Sprache zurückgegeben, einschließlich aller lokalisierten Namen. <br/>                                                                                       |
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familienliste oder tag cloud verwendet werden können. Werte werden gemäß der Sprachliste in der Reihenfolge ihrer Priorität zurückgegeben. Wenn eine Schriftart mehr als einen lokalisierten Namen enthält, wird der bevorzugte zurückgegeben. <br/> |
| [**GetPropertyValues(UINT32, DWRITE \_ FONT \_ PROPERTY \_ ID, BOOL \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Gibt die Eigenschaftswerte eines bestimmten Schriftartelementindexes zurück.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
