---
description: Die dvdadm. ConfirmPassword-Methode testet, ob das angegebene Kennwort mit dem zuvor gespeicherten Kennwort übereinstimmt.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: ConfirmPassword-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357705"
---
# <a name="confirmpassword-method"></a>ConfirmPassword-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDAdm.ConfirmPassword` Methode testet, ob das angegebene Kennwort mit dem zuvor gespeicherten Kennwort übereinstimmt.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den Namen des Benutzers als Zeichenfolge an.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt das neue Kennwort als Zeichenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt true zurück, wenn das angegebene Kennwort mit dem vorhandenen Kennwort übereinstimmt, andernfalls false.

## <a name="remarks"></a>Bemerkungen

Derzeit wird der *sUserName* -Parameter für dieses und alle zugehörigen Methoden ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




