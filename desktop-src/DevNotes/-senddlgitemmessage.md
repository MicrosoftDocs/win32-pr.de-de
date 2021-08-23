---
description: Sendet eine Nachricht an das angegebene Steuerelement in einem Dialogfeld.
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
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538835"
---
# <a name="_senddlgitemmessage-function"></a>\_SendDlgItemMessage-Funktion

\[Diese Funktion ist ein Wrapper für die **SendDlgItemMessage-Funktion.** Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **SendDlgItemMessage** direkt aufrufen.\]

Sendet eine Nachricht an das angegebene Steuerelement in einem Dialogfeld. Siehe [**SendDlgItemMessage.**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

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

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
