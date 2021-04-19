---
title: Extern. changeView-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die changeView-Methode ändert die Ansicht in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- changeView-Methode (Windows Media Player)
- changeView-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, changeView-Methode
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
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373596"
---
# <a name="externalchangeview-method"></a>Extern. changeView-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **changeView** -Methode ändert die Ansicht in Windows Media Player.

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

*Librarylocationtype* \[ in\]
</dt> <dd>

Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der neuen Ansicht angibt. Beispielsweise gibt die Konstante cpgenreid an, dass in der neuen Ansicht ein bestimmtes Genre angezeigt wird.

</dd> <dt>

*Librarylocationid* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die ID des bestimmten Elements enthält, das in der neuen Ansicht angezeigt werden soll. Wenn *librarylocationtype* beispielsweise cpgenreid ist, gibt dieser Parameter die ID des Genres an, das in der neuen Ansicht angezeigt werden soll. Diese Zeichenfolge kann leer sein. Siehe Hinweise.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Filter für die neue Ansicht enthält. Die Ansicht wird so gefiltert, als ob der Benutzer diesen Text im Word-Wheel-Steuerelement des Players eingegeben hätte. Diese Zeichenfolge kann leer sein.

</dd> <dt>

*Viewparametriams* \[ in\]
</dt> <dd>

**Zeichenfolge** , die Parameter enthält, die von Windows Media Player der neuen Ermittlungs Seite zur Verfügung gestellt werden, die in der neuen Ansicht angezeigt wird. Diese Parameter werden von Windows Media Player nicht interpretiert. Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In einigen Fällen ist es sinnvoll, den *librarylocationid* -Parameter auf die leere Zeichenfolge festzulegen. Wenn Sie z. b. den *librarylocationtype* -Parameter auf allcpalbumids festlegen, stellt die neue Ansicht Alle Alben dar. Kein einzelnes Album ist der Schwerpunkt der neuen Ansicht, daher ist es nicht erforderlich, eine Album-ID im *librarylocationid* -Parameter bereitzustellen.

Der *viewparameams* -Parameter bietet die Möglichkeit, eine Ermittlungs Seite mit einer anderen Ermittlungs Seite zu kommunizieren. Wenn das Skript auf einer Ermittlungs Seite **changeView** aufruft, wird die Benutzeroberfläche von Windows Media Player angepasst. Diese Anpassung bewirkt, dass der Spieler die [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode des Plug-Ins aufruft, um die URL einer neuen Ermittlungs Seite zu erhalten. Die Zeichenfolge, die die ursprüngliche Ermittlungs Seite in den *viewparameams* -Parameter übergibt, wird nicht an **GetTemplate** übergeben. Die neue Ermittlungs Seite kann jedoch die *viewparameterzeichenfolge* abrufen, indem [externe. viewparameters](external-viewparameters.md)aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. changeviewonlinelist**](external-changeviewonlinelist.md)
</dt> <dt>

[**Extern. librarylocationid**](external-librarylocationid.md)
</dt> <dt>

[**Extern. librarylocationtype**](external-librarylocationtype.md)
</dt> <dt>

[**Extern. viewparameters**](external-viewparameters.md)
</dt> </dl>

 

 





