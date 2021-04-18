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
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343864"
---
# <a name="direct2d-constants"></a>Direct2D-Konstanten

Die folgenden Konstanten werden in den `d2d1effectauthor.h` `d2d1.h` `d2d1_1.h` Header Dateien,, und deklariert `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Wird verwendet, wenn Eingabe Layout-Elemente verpackt werden. Gibt an, dass die Elemente zusammenhängend verpackt werden müssen.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
Die Standardtoleranz für geometrische Vereinfachungs Vorgänge.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Definiert einen ungültigen Eigenschafts Index.

Diese Konstante wird von [**ID2D1Properties:: getpropertyindex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) zurückgegeben, um anzugeben, dass die angegebene benannte Eigenschaft nicht über einen Index in der Eigenschaften Schnittstelle verfügt.

Wenn Sie diese Konstante an [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) oder [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32))übergeben, schlägt der-Befehl fehl, und der Ausgabepuffer wird mit Nullen gefüllt.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Bleiben Verwenden Sie nicht.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)
Die Anzahl der Nits, die von sRGB-oder ScRGB-Farbraum für SZR weiß oder Gleit Komma Werte von 1.0 f verwendet werden. Dieser Wert ist nur konstant, wenn der Farbraum die von der Szene referenzierte Leuchtkraft verwendet. Dies gilt für den Inhalt mit hohem dynamischen Bereich (HDR). Wenn für den Farbraum die Anzeige von der Anzeige verwendet wird, sollte die e/a-Ebene von der Anzeige abgefragt werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\] |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\] |
| Unterstützte Mindestversion (Telefon) | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps \] , Windows Phone 8,1 \[ Windows Phone Silverlight 8,1-und Windows-Runtime-apps\] |
| Header | d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h |
