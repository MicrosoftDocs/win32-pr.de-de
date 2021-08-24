---
title: Direct2D-Konstanten
description: Direct2D definiert die folgende Liste von Konstanten.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: cd8adfa3d6fa3c59a05331c82ea12100918a4697d9478097a890eedff039d5e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768730"
---
# <a name="direct2d-constants"></a>Direct2D-Konstanten

Die folgenden Konstanten werden in den `d2d1effectauthor.h` `d2d1.h` Headerdateien , `d2d1_1.h` , und `d2d1effects_2.h` deklariert.

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Wird beim Packen von Eingabelayoutelementen verwendet. Sie gibt an, dass die Elemente zusammenhängend gepackt werden müssen.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25f)
Die Standardtoleranz für geometrische Flatteningvorgänge.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Definiert einen ungültigen Eigenschaftenindex.

Diese Konstante wird von [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) zurückgegeben, um anzugeben, dass die angegebene benannte Eigenschaft keinen Index in der Eigenschaftenschnittstelle hat.

Wenn Sie diese Konstante an [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) oder [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32))übergeben, schlägt der Aufruf fehl, und der Ausgabepuffer ist null gefüllt.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Reserviert; nicht verwenden.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)
Die Anzahl der Nits, die der sRGB- oder scRGB-Farbraum für SDR-Weiß oder Gleitkommawerte von 1,0f verwendet. Dieser Wert ist nur konstant, wenn der Farbraum szenenverwiesene Leuchtdichte verwendet, was für HDR-Inhalte (High Dynamic Range) zutrifft. Wenn der Farbraum stattdessen die anzeigebezogene Leuchtdichte verwendet, sollte der SDR-Weißgrad von der Anzeige abgefragt werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 7 Windows Vista mit SP2 und Plattformupdate für UWP-Apps für Windows \[ \| Vista-Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server \[ 2008-Desktop-Apps \| UWP-Apps\] |
| Unterstützte Mindestversion (Telefon) | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps \] Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\] |
| Header | d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h |
