---
title: Extern. SendMessage-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die SendMessage-Methode sendet eine Nachricht an das Plug-in des Online Stores.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- SendMessage-Methode (Windows Media Player)
- SendMessage-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, SendMessage-Methode
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353008"
---
# <a name="externalsendmessage-method"></a>Extern. SendMessage-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **SendMessage** -Methode sendet eine Nachricht an das Plug-in des Online Stores.

## <a name="syntax"></a>Syntax


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 Meldung \[ in\]
</dt> <dd>

**Zeichenfolge** , die die Meldung enthält.

</dd> <dt>

*Param* \[ in\]
</dt> <dd>

**Zeichenfolge** mit Parametern, die der Meldung zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Nachricht wird asynchron gesendet. Das heißt, dass diese Methode sofort zurückgegeben wird, anstatt darauf zu warten, dass die Nachricht verarbeitet wird. Wenn das Plug-in die Verarbeitung der Nachricht abgeschlossen hat, ruft es die [iwmpcontentpartnercallback:: sendmessagecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) -Methode auf, die wiederum den [onsendmessagecomplete](external-onsendmessagecomplete-event.md) -Ereignishandler des Skripts aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. onsendmessagecomplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**Iwmpcontentpartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**Iwmpcontentpartnercallback:: sendmessagecomplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





