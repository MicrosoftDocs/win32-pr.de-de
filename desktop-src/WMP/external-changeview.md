---
title: External.changeView-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die changeView-Methode ändert die Ansicht in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- changeView-Windows Media Player
- changeView-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , changeView-Methode
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa982e87e0a25fa8ae6cc80b428524844f60e2ec76f50d246e7b2a76b3ca942a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649370"
---
# <a name="externalchangeview-method"></a>External.changeView-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **changeView-Methode** ändert die Ansicht in Windows Media Player.

## <a name="syntax"></a>Syntax


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LibraryLocationType* \[ In\]
</dt> <dd>

Eine [Bibliotheksspeicherort-Konstante,](library-location-constants.md) die den Typ der neuen Ansicht angibt. Beispielsweise gibt die Konstante CPGenreID an, dass die neue Ansicht ein bestimmtes Genre zeigt.

</dd> <dt>

*LibraryLocationID* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die die ID des bestimmten Elements enthält, das in der neuen Ansicht angezeigt werden soll. Wenn *LibraryLocationType* beispielsweise CPGenreID ist, gibt dieser Parameter die ID des Genre an, das in der neuen Ansicht angezeigt werden soll. Diese Zeichenfolge kann leer sein. Siehe Hinweise.

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Filter für die neue Sicht enthält. Die Ansicht wird gefiltert, als ob der Benutzer diesen Text in das Wortrad-Steuerelement des Players eingegeben hätte. Diese Zeichenfolge kann leer sein.

</dd> <dt>

*ViewParams* \[ In\]
</dt> <dd>

**Zeichenfolge** mit Parametern, Windows Media Player der neuen Ermittlungsseite zur Verfügung gestellt werden, die mit der neuen Ansicht angezeigt wird. Diese Parameter werden von der -Windows Media Player. Sie werden vom Onlineshop erstellt und haben nur eine Bedeutung für den Onlineshop.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In einigen Fällen ist es sinnvoll, den *LibraryLocationID-Parameter* auf die leere Zeichenfolge zu setzen. Wenn Sie beispielsweise den *Parameter LibraryLocationType* auf AllCPTeriIDs festlegen, stellt die neue Ansicht alle Albums dar. Kein einzelnes Album wird der Fokus der neuen Ansicht sein, sodass im *Parameter LibraryLocationID* keine Album-ID angegeben werden muss.

Der *ViewParams-Parameter* bietet einer Ermittlungsseite die Möglichkeit, mit einer anderen Ermittlungsseite zu kommunizieren. Wenn das Skript auf einer Ermittlungsseite **changeView aufruft,** Windows Media Player Die Benutzeroberfläche wird angepasst. Diese Anpassung bewirkt, dass der Player die [IWMPContentPartner::GetTemplate-Methode](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) des Plug-Ins aufruft, um die URL einer neuen Ermittlungsseite zu erhalten. Die Zeichenfolge, die die ursprüngliche Ermittlungsseite im *ViewParams-Parameter* übergibt, wird nicht an **GetTemplate übergeben.** Die neue Ermittlungsseite kann jedoch die *ViewParams-Zeichenfolge* abrufen, indem [External.viewParameters aufgerufen wird.](external-viewparameters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





