---
title: External.OnViewChange-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das OnViewChange-Ereignis tritt auf, wenn sich die Ansicht in Windows Media Player ändert.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- External.OnViewChange-Ereignis Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c01db02ef1bfd194330483c8dd7e71eba7ed09d9b347aee4b4813f413950c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648680"
---
# <a name="externalonviewchange-event"></a>External.OnViewChange-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnViewChange-Ereignis** tritt auf, wenn sich die Ansicht in Windows Media Player ändert.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, die Windows Media Player aufruft, wenn das Ereignis auftritt.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Hinweise

Die Ansicht in Windows Media Player kann sich aus einem der folgenden Gründe ändern:

-   Der Benutzer interagiert mit der Windows Media Player Benutzeroberfläche.
-   Der Benutzer interagiert mit einer Ermittlungsseite, und das Skript auf der Ermittlungsseite ruft [External.changeView](external-changeview.md)auf.
-   Der Benutzer interagiert mit einer Ermittlungsseite, und das Skript auf der Ermittlungsseite ruft [External.changeViewOnlineList](external-changeviewonlinelist.md)auf.

Wenn sich die Ansicht in Windows Media Player ändert, ruft der Player [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) auf, um die URL der nächsten anzuzeigenden Ermittlungsseite abzurufen. Bevor der Player jedoch die neue Ermittlungsseite anzeigt, löst er das **OnViewChange-Ereignis** aus. Wenn der **OnViewChange-Ereignishandler** [External.cancelNavigate](external-cancelnavigate.md)aufruft, zeigt Windows Media Player die neue Ermittlungsseite nicht an. Stattdessen wird weiterhin die aktuelle Ermittlungsseite angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





