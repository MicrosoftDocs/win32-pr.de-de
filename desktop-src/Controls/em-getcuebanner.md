---
title: EM_GETCUEBANNER Meldung (kommstrg. h)
description: Ruft den Text ab, der als Text Hinweis oder Tipp in einem Bearbeitungs Steuerelement angezeigt wird.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Windows-Steuerelemente für EM_GETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957147"
---
# <a name="em_getcuebanner-message"></a>EM \_ getcuebanner-Meldung

Ruft den Text ab, der als Text Hinweis oder Tipp in einem Bearbeitungs Steuerelement angezeigt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Unicode-Puffer, der den Text erhält, der als Text Hinweis festgelegt ist. Der Aufrufer ist für die Zuordnung des Puffers verantwortlich.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den von *wParam* in **WCHARs** verwiesen wird, einschließlich des abschließenden **null**-Werte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Getcuebannertext bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





