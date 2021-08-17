---
title: LVM_GETCOLUMN (Commctrl.h)
description: Ruft die Attribute der Spalte eines Listenansicht-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetColumn-Makros senden.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411736"
---
# <a name="lvm_getcolumn-message"></a>LVM \_ GETCOLUMN-Nachricht

Ruft die Attribute der Spalte eines Listenansicht-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetColumn-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**LVCOLUMN-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) der die Informationen zum Abrufen und Empfangen von Informationen über die Spalte angibt. Das **Maskenmitglied** gibt an, welche Spaltenattribute abgerufen werden. Wenn der **Maskenelement** den LVCF TEXT-Wert angibt, muss der pszText-Member die Adresse des Puffers enthalten, der den Elementtext empfängt, und der \_ **cchTextMax-Member** muss die Größe des Puffers angeben. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





