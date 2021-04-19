---
description: Sendet eine Meldung an das angegebene Steuerelement in einem Dialogfeld.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365964"
---
# <a name="_senddlgitemmessage-function"></a>\_SendDlgItemMess-Funktion

\[Diese Funktion ist ein Wrapper über die **SendDlgItemMess** -Funktion. Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **SendDlgItemMess** direkt aufzurufen.\]

Sendet eine Meldung an das angegebene Steuerelement in einem Dialogfeld. Siehe [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).

## <a name="syntax"></a>Syntax


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SendDlgItemMess age**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
