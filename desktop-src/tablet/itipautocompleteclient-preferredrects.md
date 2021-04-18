---
description: Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: Itipaudecompleteclient::P referredrects-Methode (tipaudecomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347725"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>Itipaudecompleteclient::P referredrects-Methode

Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prcaclist* \[ in\]
</dt> <dd>

Ein Rechteck in Bildschirm Koordinaten, das den bevorzugten Speicherort des Anbieters und die Größe der Benutzeroberfläche für die automatische vollständige Liste angibt.

</dd> <dt>

*prcfield* \[ in\]
</dt> <dd>

Ein Rechteck in Bildschirm Koordinaten, das die Position und die Größe des Fokus Felds angibt.

</dd> <dt>

*prcmodified* \[ vorgenommen\]
</dt> <dd>

Ein Rechteck, das auf dem aktuellen Status des Tipps und dem bevorzugten, durch *prcaclist* angegebenen Speicherort für die automatische Vervollständigung und Größe basiert.

</dd> <dt>

*pfshownabovetip* \[ in, out\]
</dt> <dd>

**True** , wenn das geänderte Rechteck über dem Zielbereich des Text Eintrags angezeigt werden soll. andernfalls **false**. Dieser Wert muss mit der bevorzugten Ausrichtung des Anbieters initialisiert werden, bevor die-Methode aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Rufen Sie die [**itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md) auf, um das Popup Fenster für das automatische vollständige Popup Fenster vor dem Aufrufen der [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)festzulegen.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Es ist ein unbekannter Fehler aufgetreten.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Dies ist die Methode, die der Auto Vervollständigen-Anbieter aufruft, wenn die automatische Vervollständigung der Benutzeroberfläche angezeigt wird. Der Client ändert das bevorzugte Rechteck des Anbieters, das durch *prcaclist* über das *prcmodified* -Argument angegeben wird.

Aufrufen der [**itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md) , um das Fenster Handle für die automatische Vervollständigung des Popups vor dem Aufrufen von **preferredrects** festzulegen. Wenn dies nicht der Fall ist, wird beim Aufrufen von " **preferredrects**" ein **E \_ invalidArg** -Fehler ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itipauwebcompleteclient-Schnittstelle**](itipautocompleteclient.md)
</dt> <dt>

[**Itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




