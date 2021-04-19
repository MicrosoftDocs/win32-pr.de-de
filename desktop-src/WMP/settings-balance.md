---
title: Einstellungen. Balance
description: Die Balance-Eigenschaft gibt den aktuellen Stereo Saldo an oder ruft ihn ab.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Einstellungen. Balance für Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359249"
---
# <a name="settingsbalance"></a>Einstellungen. Balance

Die **Balance** -Eigenschaft gibt den aktuellen Stereo Saldo an oder ruft ihn ab.

## <a name="syntax"></a>Syntax

Player. Settings. Balance

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**).  Die Werte liegen im Bereich von 100 bis 100. der Standardwert ist 0 (null).

## <a name="remarks"></a>Bemerkungen

Der Wert 0 (null) gibt an, dass die Audiodaten gleichzeitig auf dem linken und rechten Kanal abgespielt werden. Der Wert 100 gibt an, dass Audioinhalte nur im linken Kanal abgespielt werden. Der Wert 100 gibt an, dass Audioinhalte nur auf dem rechten Kanal abgespielt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 





