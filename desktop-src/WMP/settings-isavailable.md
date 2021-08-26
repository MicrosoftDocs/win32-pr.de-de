---
title: Einstellungen.isAvailable
description: Die isAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann. | Einstellungen.isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Einstellungen.isAvailable Windows Media Player
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
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002410"
---
# <a name="settingsisavailable"></a>Einstellungen.isAvailable

Die **isAvailable-Eigenschaft** gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.

## <a name="syntax"></a>Syntax

player.settings.isAvailable( name )

## <a name="parameters"></a>Parameter

*name*

Zeichenfolge, die einen der folgenden Werte enthält.



| Zeichenfolge             | Beschreibung                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | Bestimmt, ob die autoStart-Eigenschaft festgelegt werden kann.          |
| Balance            | Bestimmt, ob die Balance-Eigenschaft festgelegt werden kann.            |
| BaseURL            | Bestimmt, ob die baseURL-Eigenschaft festgelegt werden kann.            |
| DefaultFrame       | Bestimmt, ob die defaultFrame-Eigenschaft festgelegt werden kann.       |
| EnableErrorDialogs | Bestimmt, ob die enableErrorDialogs-Eigenschaft festgelegt werden kann. |
| GetMode            | Bestimmt, ob die getMode-Methode aufgerufen werden kann.           |
| InvokeURLs         | Bestimmt, ob die invokeURLs-Eigenschaft festgelegt werden kann.         |
| Mute               | Bestimmt, ob die Stummschaltungseigenschaft festgelegt werden kann.               |
| PlayCount          | Bestimmt, ob die playCount-Eigenschaft festgelegt werden kann.          |
| Rate               | Bestimmt, ob die Rate-Eigenschaft festgelegt werden kann.               |
| SetMode            | Bestimmt, ob die setMode-Methode aufgerufen werden kann.           |
| Volume             | Bestimmt, ob die Volumeeigenschaft festgelegt werden kann.             |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> </dl>

 

 





