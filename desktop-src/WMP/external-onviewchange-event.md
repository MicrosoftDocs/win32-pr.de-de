---
title: Externes. OnViewChange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das OnViewChange-Ereignis tritt auf, wenn sich die Sicht in Windows Media Player ändert.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Externe. OnViewChange-Ereignisfenster Media Player
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
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369546"
---
# <a name="externalonviewchange-event"></a>Externes. OnViewChange-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **OnViewChange** -Ereignis tritt auf, wenn sich die Sicht in Windows Media Player ändert.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Bemerkungen

Die Ansicht in Windows Media Player kann aus einem der folgenden Gründe geändert werden:

-   Der Benutzer interagiert mit der Windows Media Player-Benutzeroberfläche.
-   Der Benutzer interagiert mit einer Ermittlungs Seite, und das Skript auf der Ermittlungs Seite ruft [extern. changeView](external-changeview.md)auf.
-   Der Benutzer interagiert mit einer Ermittlungs Seite, und das Skript auf der Ermittlungs Seite ruft [extern. changeviewonlinelist](external-changeviewonlinelist.md)auf.

Wenn sich die Ansicht in Windows Media Player ändert, ruft der Player [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) auf, um die URL der nächsten Ermittlungs Seite anzuzeigen, die angezeigt werden soll. Bevor der Spieler jedoch die neue Ermittlungs Seite anzeigt, löst er das **OnViewChange** -Ereignis aus. Wenn der **OnViewChange** -Ereignishandler " [extern. cancelnavigate](external-cancelnavigate.md)" aufruft, zeigt Windows Media Player die Seite "neue Ermittlung" nicht an. Stattdessen wird die aktuelle Ermittlungs Seite weiterhin angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. changeView**](external-changeview.md)
</dt> <dt>

[**Extern. changeviewonlinelist**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





