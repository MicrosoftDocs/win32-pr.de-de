---
description: 'Gibt das ungefilterte Bild frei, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird. Außerdem wird der Bild Verarbeitungs Filter freigegeben.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Iwiapreview:: Clear-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348790"
---
# <a name="iwiapreviewclear-method"></a>Iwiapreview:: Clear-Methode

Gibt das ungefilterte Bild frei, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird. Außerdem wird der Bild Verarbeitungs Filter freigegeben.

## <a name="syntax"></a>Syntax


```C++
void Clear();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Auf **iwiapreview:: Clear** die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente gibt alle Schnittstellen Zeiger frei, die Sie speichert. Die WIA 2,0-Vorschau Komponente behält Verweise auf *pWiaItem2* und *pwiatransfercallback* bei, die an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben werden. Um genau zu sein, behält die WIA 2,0-Vorschau Komponente einen Verweis auf *pWiaItem2* und den Bild Verarbeitungs Filter des Treibers bei, der wiederum einen Verweis auf *pwiatransfercallback* beibehält. Bei **iwiapreview:: Clear** gibt die WIA 2,0 Preview-Komponente auch Ihren Verweis auf *pWiaItem2* und den Bild Verarbeitungs Filter frei, der wiederum den Verweis auf *pwiatransfercallback* freigibt. Die WIA 2,0-Vorschau Komponente löscht das zwischengespeicherte, ungefilterte Image, das intern gespeichert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




