---
title: DVD. Back-Methode
description: Die Methode "Back" gibt die Anzeige von einem Untermenü an das übergeordnete Menü zurück.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- Windows-Media Player der Back-Methode
- Back-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, Back-Methode
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391916"
---
# <a name="dvdback-method"></a>DVD. Back-Methode

Die Methode " **Back** " gibt die Anzeige von einem Untermenü an das übergeordnete Menü zurück.

## <a name="syntax"></a>Syntax


```JScript
DVD.back()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Einige DVDs werden so erstellt, dass die **Back** -Methode über das Root-Menü verfügbar ist, aber wenn Sie aufgerufen wird, wird keine Aktion durchführen.

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





