---
title: LVM_SETINFOTIP Meldung (kommstrg. h)
description: Legt den QuickInfo-Text in verzögerter Antwort auf die LVN \_ getinfotip-Benachrichtigung fest.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Windows-Steuerelemente für LVM_SETINFOTIP Meldung
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339310"
---
# <a name="lvm_setinfotip-message"></a>LVM- \_ Nachricht

Legt den QuickInfo-Text in verzögerter Antwort auf die [LVN \_ getinfotip](lvn-getinfotip.md) -Benachrichtigung fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">lvsetinfotip</a> -Struktur, die die festzulegenden Informationen enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der QuickInfo-Text erfolgreich festgelegt wurde, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die **LVM \_ setinfotip** -Nachricht ermöglicht einer Anwendung das Berechnen von Infotipps im Hintergrund, indem die folgenden Schritte ausgeführt werden:

1.  Legen Sie als Antwort auf die [LVN \_ getinfotip](lvn-getinfotip.md) -Benachrichtigung den **pszText** -Member der [**nmlvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) -Struktur auf eine leere Zeichenfolge fest, und geben Sie 0 zurück.
2.  Im Hintergrund berechnen Sie den infotip.
3.  Nachdem Sie den Infotipp berechnet haben, senden Sie die LVM-Nachricht " **\_ stinfotip** ". Legen Sie dabei den **pszText** -Member der " [**LV* tinfotip**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) "-Struktur auf die Infotipp-und die **iItem** -und **iSubItem** -Elemente auf das Element und das Unterelement fest, für das der Infotipp gilt

Der Text, der an die LVM-Nachricht " **mesfotip \_** " weitergeleitet wird, wird nur angezeigt, wenn sich das von der Struktur " [**LV* tinfotip**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) " beschriebene Element und Unterelement noch in einem Zustand befinden, der einen InfoTipp erfordert

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





