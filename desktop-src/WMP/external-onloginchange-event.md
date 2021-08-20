---
title: External.OnLoginChange-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.OnLoginChange-Ereignis
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- External.OnLoginChange-Windows Media Player
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
ms.openlocfilehash: a0697aff759309bc3a988e6f24a024d5c05bd8ec27dae85921ee09d3847f3dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648740"
---
# <a name="externalonloginchange-event"></a>External.OnLoginChange-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnLoginChange-Ereignis** tritt auf, wenn sich der Anmeldestatus des Benutzers ändert oder ein Anmeldeversuch fehlschlägt.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, Windows Media Player beim Auftreten des Ereignisses aufruft.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt jedes Mal auf, wenn das Plug-In des Onlineshops [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)aufruft und wmpcnLoginStateChange im Typparameter *übergibt.* Manchmal wird durch das Plug-In dieser Aufruf Windows Media Player, dass sich der Anmeldezustand des Benutzers geändert hat. In anderen Zeiten wird vom Plug-In dieser Aufruf unternommen, um den Player darüber zu benachrichtigen, dass ein Anmeldeversuch fehlgeschlagen ist. Der *pContext-Parameter* der **Notify-Methode** gibt an, ob die Benachrichtigung für eine Änderung des Anmeldestatus oder für einen fehlgeschlagenen Anmeldeversuch bestimmt ist.

Da jeder Aufruf von bewirkt, dass Windows Media Player das `Notify(wmpcnLoginStateChange, ...)` **OnLoginChange-Ereignis** ausruft, wird der **OnLoginChange-Ereignishandler** manchmal als Ergebnis einer Änderung des Anmeldezustands und manchmal als Ergebnis eines fehlgeschlagenen Anmeldeversuchs aufgerufen. Um den aktuellen Anmeldezustand des Benutzers zu bestimmen, muss der **OnLoginChange-Ereignishandler** [External.userLoggedIn aufrufen.](external-userloggedin.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





