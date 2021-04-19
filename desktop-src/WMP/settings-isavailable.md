---
title: Settings. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | Settings. IsAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- "\"Settings. IsAvailable\"-Windows-Media Player"
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370660"
---
# <a name="settingsisavailable"></a>Settings. IsAvailable

Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.

## <a name="syntax"></a>Syntax

Player. Settings. IsAvailable (Name)

## <a name="parameters"></a>Parameter

*name*

Eine Zeichenfolge, die einen der folgenden Werte enthält.



| Zeichenfolge             | Beschreibung                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | Bestimmt, ob die Autostart-Eigenschaft festgelegt werden kann.          |
| Balance            | Bestimmt, ob die Balance-Eigenschaft festgelegt werden kann.            |
| Basis            | Bestimmt, ob die baseurl-Eigenschaft festgelegt werden kann.            |
| Defaultframe       | Bestimmt, ob die defaultframe-Eigenschaft festgelegt werden kann.       |
| Enableerrordialogfelder | Bestimmt, ob die enableerrordialogs-Eigenschaft festgelegt werden kann. |
| GetMode            | Bestimmt, ob die getMode-Methode aufgerufen werden kann.           |
| Invokeurls         | Bestimmt, ob die invokeurls-Eigenschaft festgelegt werden kann.         |
| Mute               | Bestimmt, ob die stumm Eigenschaft festgelegt werden kann.               |
| Playcount          | Bestimmt, ob die playcount-Eigenschaft festgelegt werden kann.          |
| Rate               | Bestimmt, ob die Raten Eigenschaft festgelegt werden kann.               |
| SetMode            | Bestimmt, ob die setmode-Methode aufgerufen werden kann.           |
| Lautstärke             | Bestimmt, ob die Volumeeigenschaft festgelegt werden kann.             |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 





