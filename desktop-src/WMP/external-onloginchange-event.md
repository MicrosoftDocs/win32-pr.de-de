---
title: Externes. onloginchange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onloginchange-Ereignis
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Externe. onloginchange-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355887"
---
# <a name="externalonloginchange-event"></a>Externes. onloginchange-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **onloginchange** -Ereignis tritt auf, wenn der Anmeldestatus des Benutzers geändert wird oder wenn der Anmeldeversuch fehlschlägt.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt jedes Mal auf, wenn das Plug-in des Online Stores [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)aufruft und dabei wmpcnloginstatechange im *Typparameter* übergibt. Manchmal führt das Plug-in diesen Rückruf aus, um Windows Media Player zu benachrichtigen, dass es eine Änderung des Anmelde Zustands des Benutzers gab. In anderen Zeiten führt das Plug-in diesen Versuch aus, den Player zu benachrichtigen, dass ein Anmeldeversuch fehlgeschlagen ist. Der *pContext* -Parameter der **Notify** -Methode gibt an, ob die Benachrichtigung für eine Änderung des Anmelde Zustands oder für einen fehlgeschlagenen Anmeldeversuch vorliegt.

Da jeder Aufruf von `Notify(wmpcnLoginStateChange, ...)` bewirkt, dass Windows Media Player das **onloginchange** -Ereignis auslöst, wird der **onloginchange** -Ereignishandler manchmal als Ergebnis einer Änderung des Anmelde Zustands aufgerufen und manchmal als Ergebnis eines fehlgeschlagenen Anmelde Versuchs. Um den aktuellen Anmeldestatus des Benutzers zu bestimmen, muss der **onloginchange** -Ereignishandler [extern. userloggedin](external-userloggedin.md)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern.-Anmelde Name**](external-attemptlogin.md)
</dt> <dt>

[**Extern. userloggedin**](external-userloggedin.md)
</dt> </dl>

 

 





