---
description: Fügt dem InkDivider-Objekt ein neues IInkStrokeDisp-Objekt hinzu, das weitergegeben wurde.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Addonestroke-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483998"
---
# <a name="addonestroke-function"></a>Addonestroke-Funktion

Fügt dem [**InkDivider**](inkdivider-class.md) -Objekt ein neues [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt hinzu, das weitergegeben wurde.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdivider* \[ in\]
</dt> <dd>

Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.

</dd> <dt>

*strokeid* \[ in\]
</dt> <dd>

Die [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts, das dem [**InkDivider**](inkdivider-class.md) -Objekt hinzugefügt werden soll.

</dd> <dt>

*CPoints* \[ in\]
</dt> <dd>

Die Anzahl der Pakete, die das neue [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt bilden.

</dd> <dt>

*apoints* \[ in\]
</dt> <dd>

Das Array von Paketen, die das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt in *strokeid* bilden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *hdivider* -Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




