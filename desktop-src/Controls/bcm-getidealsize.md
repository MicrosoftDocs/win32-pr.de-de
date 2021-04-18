---
title: BCM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die Größe der Schaltfläche ab, die den Text und das Bild am besten anpasst, wenn eine Bildliste vorhanden ist. Sie können diese Nachricht explizit senden oder das \_ getidealsize-Makro der Schaltfläche verwenden.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Windows-Steuerelemente für BCM_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339570"
---
# <a name="bcm_getidealsize-message"></a>BCM- \_ getidealsize-Meldung

Ruft die Größe der Schaltfläche ab, die den Text und das Bild am besten anpasst, wenn eine Bildliste vorhanden ist. Sie können diese Nachricht explizit senden oder das [**\_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) -Makro der Schaltfläche verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die gewünschte Größe der Schaltfläche erhält, einschließlich Text und Bildliste, falls vorhanden. Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich. Legen Sie die Member **CX** und **CY** auf NULL fest, um die ideale Höhe und Breite in der **Größen** Struktur zurückzugeben. Zum Angeben einer Schaltflächen breite legen Sie den **CX** -Member auf die gewünschte Schaltflächen Breite fest. Das System berechnet die ideale Höhe für diese Breite und gibt Sie im **CY** -Element zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Wenn keine spezielle Schaltflächen breite gewünscht ist, müssen Sie beide Member der [**Größe**](/previous-versions//dd145106(v=vs.85)) auf NULL festlegen, um die ideale Höhe und Breite zu berechnen und zurückzugeben. Wenn der Wert des **CX** -Members größer als 0 (null) ist, wird dieser Wert als gewünschte Schaltflächen breite betrachtet, und die ideale Höhe für diese Breite wird berechnet und im **CY** -Element zurückgegeben.

 

Diese Meldung ist am häufigsten auf Pushbuttons anwendbar. Beim Senden an einen PUSHBUTTON Ruft die Nachricht das umgebende Rechteck ab, das zum Anzeigen des Schaltflächen Texts erforderlich ist. Wenn der PUSHBUTTON außerdem eine Bildliste aufweist, wird das umgebende Rechteck ebenfalls so vergrößert, dass es das Bild der Schaltfläche enthält.

Beim Senden an eine Schaltfläche eines beliebigen anderen Typs wird die Größe des Fenster Rechtecks des Steuer Elements abgerufen.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

